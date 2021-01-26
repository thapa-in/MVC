1. Web.config causing "blocked by group policy" error
    * Remove all codes between  <system.codedom> tag
```
  <system.codedom>
    <compilers>
      <compiler language="c#;cs;csharp" extension=".cs" type="Microsoft.CodeDom.Providers.DotNetCompilerPlatform.CSharpCodeProvider, Microsoft.CodeDom.Providers.DotNetCompilerPlatform, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35" warningLevel="4" compilerOptions="/langversion:6 /nowarn:1659;1699;1701" />
    </compilers>
  </system.codedom>
```
    * add following code in web.config
```
<customErrors mode="Off" />
<trust level="Full" />
<authentication mode="None" />
```
2. The type 'System.Object' is defined in an assembly that is not referenced. You must add a reference to assembly 'System.Runtime, Version=4.0.0.0,
    * Replace compilation tag to 
```xml 
<compilation debug="true" targetFramework="4.5">
  <assemblies>
    <add assembly="System.Runtime, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a" />
  </assemblies>
</compilation>
```
3.
  


