---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/new-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
ms.openlocfilehash: ecb5b1200bacab12f7715600b7fcf60b78b81092
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905458"
---
# <span data-ttu-id="178c4-101">New-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="178c4-101">New-AzWvdMsixPackage</span></span>

## <span data-ttu-id="178c4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="178c4-102">SYNOPSIS</span></span>
<span data-ttu-id="178c4-103">建立或更新 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="178c4-103">Create or update a MSIX package.</span></span>

## <span data-ttu-id="178c4-104">語法</span><span class="sxs-lookup"><span data-stu-id="178c4-104">SYNTAX</span></span>

### <span data-ttu-id="178c4-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="178c4-105">CreateExpanded (Default)</span></span>
```
New-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-LastUpdated <DateTime>] [-PackageApplication <IMsixPackageApplications[]>]
 [-PackageDependency <IMsixPackageDependencies[]>] [-PackageFamilyName <String>] [-PackageName <String>]
 [-PackageRelativePath <String>] [-Version <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="178c4-106">PackageAlias</span><span class="sxs-lookup"><span data-stu-id="178c4-106">PackageAlias</span></span>
```
New-AzWvdMsixPackage -HostPoolName <String> -PackageAlias <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="178c4-107">描述</span><span class="sxs-lookup"><span data-stu-id="178c4-107">DESCRIPTION</span></span>
<span data-ttu-id="178c4-108">建立或更新 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="178c4-108">Create or update a MSIX package.</span></span>

## <span data-ttu-id="178c4-109">例子</span><span class="sxs-lookup"><span data-stu-id="178c4-109">EXAMPLES</span></span>

### <span data-ttu-id="178c4-110">範例 1：透過套件別名在 HostPool 中建立新的 MSIX 套件</span><span class="sxs-lookup"><span data-stu-id="178c4-110">Example 1: Creates New MSIX Package in the HostPool via Package Alias</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
      -PackageAlias packagealias `
      -ImagePath ImagePathURI  `
```

<span data-ttu-id="178c4-111">此命令會將 MSIX 套件從指定的圖像路徑新增到 HostPool</span><span class="sxs-lookup"><span data-stu-id="178c4-111">This command adds MSIX package from specified image path to HostPool</span></span>

### <span data-ttu-id="178c4-112">範例 2：在 HostPool 中建立新 MSIX 套件</span><span class="sxs-lookup"><span data-stu-id="178c4-112">Example 2: Creates New MSIX Package in the HostPool</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -FullName PackageFullName `
                            -HostPoolName HostPoolName `
                            -ResourceGroupName ResourceGroupName ` 
                            -SubscriptionId SubscriptionId ` 
                            -DisplayName displayname `
                            -ImagePath imageURI ` 
                            -IsActive:$false `
                            -IsRegularRegistration:$false `
                            -LastUpdated datelastupdated `
                            -PackageApplication $apps `
                            -PackageDependency $deps `
                            -PackageFamilyName packagefamilyname `
                            -PackageName packagename `
                            -PackageRelativePath packagerelativepath `
                            -Version packageversion `

Name                              Type
----                              ----
HotPoolName/PackageFullName      Microsoft.DesktopVirtualization/hostpools/msixpackages

```

<span data-ttu-id="178c4-113">此命令會新增指定 HostPool 中的 MSIX 套件</span><span class="sxs-lookup"><span data-stu-id="178c4-113">This command adds MSIX Package in the specified HostPool</span></span>

## <span data-ttu-id="178c4-114">參數</span><span class="sxs-lookup"><span data-stu-id="178c4-114">PARAMETERS</span></span>

### <span data-ttu-id="178c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="178c4-115">-DefaultProfile</span></span>
<span data-ttu-id="178c4-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="178c4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c4-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="178c4-117">-DisplayName</span></span>
<span data-ttu-id="178c4-118">要顯示在入口網站中的使用者好用名稱。</span><span class="sxs-lookup"><span data-stu-id="178c4-118">User friendly Name to be displayed in the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c4-119">-FullName</span><span class="sxs-lookup"><span data-stu-id="178c4-119">-FullName</span></span>
<span data-ttu-id="178c4-120">指定主機多工緩衝處理程式中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="178c4-120">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c4-121">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="178c4-121">-HostPoolName</span></span>
<span data-ttu-id="178c4-122">指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="178c4-122">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c4-123">-ImagePath</span><span class="sxs-lookup"><span data-stu-id="178c4-123">-ImagePath</span></span>
<span data-ttu-id="178c4-124">網路共用上的 VHD/CIM 圖像路徑。</span><span class="sxs-lookup"><span data-stu-id="178c4-124">VHD/CIM image path on Network Share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c4-125">-IsActive</span><span class="sxs-lookup"><span data-stu-id="178c4-125">-IsActive</span></span>
<span data-ttu-id="178c4-126">讓此版本的套件在主機主機上成為使用中版本。</span><span class="sxs-lookup"><span data-stu-id="178c4-126">Make this version of the package the active one across the hostpool.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c4-127">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="178c4-127">-IsRegularRegistration</span></span>
<span data-ttu-id="178c4-128">指定如何在進紙中註冊 Package。</span><span class="sxs-lookup"><span data-stu-id="178c4-128">Specifies how to register Package in feed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c4-129">-LastUpdated</span><span class="sxs-lookup"><span data-stu-id="178c4-129">-LastUpdated</span></span>
<span data-ttu-id="178c4-130">上次更新的日期套件，請見appxmanifest.xml。</span><span class="sxs-lookup"><span data-stu-id="178c4-130">Date Package was last updated, found in the appxmanifest.xml.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c4-131">-PackageAlias</span><span class="sxs-lookup"><span data-stu-id="178c4-131">-PackageAlias</span></span>
<span data-ttu-id="178c4-132">從解壓縮 MSIX 影像的套件別名</span><span class="sxs-lookup"><span data-stu-id="178c4-132">Package Alias from extract MSIX Image</span></span>

```yaml
Type: System.String
Parameter Sets: PackageAlias
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c4-133">-PackageApplication</span><span class="sxs-lookup"><span data-stu-id="178c4-133">-PackageApplication</span></span>
<span data-ttu-id="178c4-134">套件應用程式清單。</span><span class="sxs-lookup"><span data-stu-id="178c4-134">List of package applications.</span></span>

<span data-ttu-id="178c4-135">若要建構，請參閱 PACKAGEAPPLICATION 屬性的附注區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="178c4-135">To construct, see NOTES section for PACKAGEAPPLICATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackageApplications[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c4-136">-PackageDependency</span><span class="sxs-lookup"><span data-stu-id="178c4-136">-PackageDependency</span></span>
<span data-ttu-id="178c4-137">套件相依性清單。</span><span class="sxs-lookup"><span data-stu-id="178c4-137">List of package dependencies.</span></span>

<span data-ttu-id="178c4-138">若要建構，請參閱有關 PACKAGEDEPENDENCY 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="178c4-138">To construct, see NOTES section for PACKAGEDEPENDENCY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackageDependencies[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c4-139">-PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="178c4-139">-PackageFamilyName</span></span>
<span data-ttu-id="178c4-140">從 appxmanifest.xml 套件appxmanifest.xml。</span><span class="sxs-lookup"><span data-stu-id="178c4-140">Package Family Name from appxmanifest.xml.</span></span>
<span data-ttu-id="178c4-141">包含套件名稱和 Publisher 名稱。</span><span class="sxs-lookup"><span data-stu-id="178c4-141">Contains Package Name and Publisher name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c4-142">-PackageName</span><span class="sxs-lookup"><span data-stu-id="178c4-142">-PackageName</span></span>
<span data-ttu-id="178c4-143">來自 appxmanifest.xml 的套件appxmanifest.xml。</span><span class="sxs-lookup"><span data-stu-id="178c4-143">Package Name from appxmanifest.xml.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c4-144">-PackageRelativePath</span><span class="sxs-lookup"><span data-stu-id="178c4-144">-PackageRelativePath</span></span>
<span data-ttu-id="178c4-145">影像內套件的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="178c4-145">Relative Path to the package inside the image.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c4-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="178c4-146">-ResourceGroupName</span></span>
<span data-ttu-id="178c4-147">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="178c4-147">The name of the resource group.</span></span>
<span data-ttu-id="178c4-148">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="178c4-148">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c4-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="178c4-149">-SubscriptionId</span></span>
<span data-ttu-id="178c4-150">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="178c4-150">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c4-151">-版本</span><span class="sxs-lookup"><span data-stu-id="178c4-151">-Version</span></span>
<span data-ttu-id="178c4-152">套件版本appxmanifest.xml。</span><span class="sxs-lookup"><span data-stu-id="178c4-152">Package Version found in the appxmanifest.xml.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c4-153">-確認</span><span class="sxs-lookup"><span data-stu-id="178c4-153">-Confirm</span></span>
<span data-ttu-id="178c4-154">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="178c4-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c4-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="178c4-155">-WhatIf</span></span>
<span data-ttu-id="178c4-156">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="178c4-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="178c4-157">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="178c4-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="178c4-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="178c4-158">CommonParameters</span></span>
<span data-ttu-id="178c4-159">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="178c4-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="178c4-160">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="178c4-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="178c4-161">輸入</span><span class="sxs-lookup"><span data-stu-id="178c4-161">INPUTS</span></span>

## <span data-ttu-id="178c4-162">輸出</span><span class="sxs-lookup"><span data-stu-id="178c4-162">OUTPUTS</span></span>

### <span data-ttu-id="178c4-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.Api20201102Preview.IMsixPackage</span><span class="sxs-lookup"><span data-stu-id="178c4-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixPackage</span></span>

## <span data-ttu-id="178c4-164">筆記</span><span class="sxs-lookup"><span data-stu-id="178c4-164">NOTES</span></span>

<span data-ttu-id="178c4-165">別名</span><span class="sxs-lookup"><span data-stu-id="178c4-165">ALIASES</span></span>

<span data-ttu-id="178c4-166">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="178c4-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="178c4-167">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="178c4-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="178c4-168">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="178c4-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="178c4-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>：套件應用程式清單。</span><span class="sxs-lookup"><span data-stu-id="178c4-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: List of package applications.</span></span> 
  - <span data-ttu-id="178c4-170">`[AppId <String>]`：套件應用程式識別碼，位於 appxmanifest.xml。</span><span class="sxs-lookup"><span data-stu-id="178c4-170">`[AppId <String>]`: Package Application Id, found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="178c4-171">`[AppUserModelId <String>]`：用來啟用套件應用程式。</span><span class="sxs-lookup"><span data-stu-id="178c4-171">`[AppUserModelId <String>]`: Used to activate Package Application.</span></span> <span data-ttu-id="178c4-172">包含套件名稱與 ApplicationID。</span><span class="sxs-lookup"><span data-stu-id="178c4-172">Consists of Package Name and ApplicationID.</span></span> <span data-ttu-id="178c4-173">位於appxmanifest.xml。</span><span class="sxs-lookup"><span data-stu-id="178c4-173">Found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="178c4-174">`[Description <String>]`：套件應用程式的描述。</span><span class="sxs-lookup"><span data-stu-id="178c4-174">`[Description <String>]`: Description of Package Application.</span></span>
  - <span data-ttu-id="178c4-175">`[FriendlyName <String>]`：使用者好用的名稱。</span><span class="sxs-lookup"><span data-stu-id="178c4-175">`[FriendlyName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="178c4-176">`[IconImageName <String>]`：使用者好用的名稱。</span><span class="sxs-lookup"><span data-stu-id="178c4-176">`[IconImageName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="178c4-177">`[RawIcon <Byte[]>]`：圖示 64 位字串作為位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="178c4-177">`[RawIcon <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>
  - <span data-ttu-id="178c4-178">`[RawPng <Byte[]>]`：圖示 64 位字串作為位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="178c4-178">`[RawPng <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>

<span data-ttu-id="178c4-179">PACKAGEEPENDENCY <IMsixPackageDependencies[]>：套件相依性清單。</span><span class="sxs-lookup"><span data-stu-id="178c4-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: List of package dependencies.</span></span> 
  - <span data-ttu-id="178c4-180">`[DependencyName <String>]`：封裝相依性的名稱。</span><span class="sxs-lookup"><span data-stu-id="178c4-180">`[DependencyName <String>]`: Name of package dependency.</span></span>
  - <span data-ttu-id="178c4-181">`[MinVersion <String>]`：相依性版本為必填專案。</span><span class="sxs-lookup"><span data-stu-id="178c4-181">`[MinVersion <String>]`: Dependency version required.</span></span>
  - <span data-ttu-id="178c4-182">`[Publisher <String>]`：相依性發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="178c4-182">`[Publisher <String>]`: Name of dependency publisher.</span></span>

## <span data-ttu-id="178c4-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="178c4-183">RELATED LINKS</span></span>

