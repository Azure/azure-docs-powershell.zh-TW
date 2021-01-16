---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdMsixPackage.md
ms.openlocfilehash: fd5dd920863d4bd53257cfe2170e83f53c620096
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281432"
---
# <span data-ttu-id="9c9da-101">New-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="9c9da-101">New-AzWvdMsixPackage</span></span>

## <span data-ttu-id="9c9da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9c9da-102">SYNOPSIS</span></span>
<span data-ttu-id="9c9da-103">建立或更新 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="9c9da-103">Create or update a MSIX package.</span></span>

## <span data-ttu-id="9c9da-104">句法</span><span class="sxs-lookup"><span data-stu-id="9c9da-104">SYNTAX</span></span>

### <span data-ttu-id="9c9da-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="9c9da-105">CreateExpanded (Default)</span></span>
```
New-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-LastUpdated <DateTime>] [-PackageApplication <IMsixPackageApplications[]>]
 [-PackageDependency <IMsixPackageDependencies[]>] [-PackageFamilyName <String>] [-PackageName <String>]
 [-PackageRelativePath <String>] [-Version <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9c9da-106">PackageAlias</span><span class="sxs-lookup"><span data-stu-id="9c9da-106">PackageAlias</span></span>
```
New-AzWvdMsixPackage -HostPoolName <String> -PackageAlias <String> -ResourceGroupName <String>
 [-DisplayName <String>] [-ImagePath <String>] [-IsActive] [-IsRegularRegistration] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9c9da-107">說明</span><span class="sxs-lookup"><span data-stu-id="9c9da-107">DESCRIPTION</span></span>
<span data-ttu-id="9c9da-108">建立或更新 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="9c9da-108">Create or update a MSIX package.</span></span>

## <span data-ttu-id="9c9da-109">示例</span><span class="sxs-lookup"><span data-stu-id="9c9da-109">EXAMPLES</span></span>

### <span data-ttu-id="9c9da-110">範例1：透過套件別名在 HostPool 中建立新的 MSIX 套件</span><span class="sxs-lookup"><span data-stu-id="9c9da-110">Example 1: Creates New MSIX Package in the HostPool via Package Alias</span></span>
```powershell
PS C:\> New-AzWvdMsixPackage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
      -PackageAlias packagealias `
      -ImagePath ImagePathURI  `
```

<span data-ttu-id="9c9da-111">這個命令會將 MSIX 套件從指定的影像路徑新增至 HostPool</span><span class="sxs-lookup"><span data-stu-id="9c9da-111">This command adds MSIX package from specified image path to HostPool</span></span>

### <span data-ttu-id="9c9da-112">範例2：在 HostPool 中建立新的 MSIX 套件</span><span class="sxs-lookup"><span data-stu-id="9c9da-112">Example 2: Creates New MSIX Package in the HostPool</span></span>
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

<span data-ttu-id="9c9da-113">這個命令會在指定的 HostPool 中新增 MSIX 套件</span><span class="sxs-lookup"><span data-stu-id="9c9da-113">This command adds MSIX Package in the specified HostPool</span></span>

## <span data-ttu-id="9c9da-114">參數</span><span class="sxs-lookup"><span data-stu-id="9c9da-114">PARAMETERS</span></span>

### <span data-ttu-id="9c9da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c9da-115">-DefaultProfile</span></span>
<span data-ttu-id="9c9da-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9c9da-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c9da-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9c9da-117">-DisplayName</span></span>
<span data-ttu-id="9c9da-118">要在入口網站中顯示的使用者易記名稱。</span><span class="sxs-lookup"><span data-stu-id="9c9da-118">User friendly Name to be displayed in the portal.</span></span>

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

### <span data-ttu-id="9c9da-119">-FullName</span><span class="sxs-lookup"><span data-stu-id="9c9da-119">-FullName</span></span>
<span data-ttu-id="9c9da-120">指定 hostpool 中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="9c9da-120">The version specific package full name of the MSIX package within specified hostpool</span></span>

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

### <span data-ttu-id="9c9da-121">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="9c9da-121">-HostPoolName</span></span>
<span data-ttu-id="9c9da-122">指定資源群組中主機池的名稱</span><span class="sxs-lookup"><span data-stu-id="9c9da-122">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="9c9da-123">-ImagePath</span><span class="sxs-lookup"><span data-stu-id="9c9da-123">-ImagePath</span></span>
<span data-ttu-id="9c9da-124">網路共用上的 VHD/CIM 影像路徑。</span><span class="sxs-lookup"><span data-stu-id="9c9da-124">VHD/CIM image path on Network Share.</span></span>

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

### <span data-ttu-id="9c9da-125">-IsActive</span><span class="sxs-lookup"><span data-stu-id="9c9da-125">-IsActive</span></span>
<span data-ttu-id="9c9da-126">將這個版本的套件製作成 hostpool 的作用中。</span><span class="sxs-lookup"><span data-stu-id="9c9da-126">Make this version of the package the active one across the hostpool.</span></span>

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

### <span data-ttu-id="9c9da-127">-IsRegularRegistration</span><span class="sxs-lookup"><span data-stu-id="9c9da-127">-IsRegularRegistration</span></span>
<span data-ttu-id="9c9da-128">指定如何在摘要中註冊套件。</span><span class="sxs-lookup"><span data-stu-id="9c9da-128">Specifies how to register Package in feed.</span></span>

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

### <span data-ttu-id="9c9da-129">-LastUpdated</span><span class="sxs-lookup"><span data-stu-id="9c9da-129">-LastUpdated</span></span>
<span data-ttu-id="9c9da-130">上次更新的日期套件，在 appxmanifest.xml 中找到。</span><span class="sxs-lookup"><span data-stu-id="9c9da-130">Date Package was last updated, found in the appxmanifest.xml.</span></span>

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

### <span data-ttu-id="9c9da-131">-PackageAlias</span><span class="sxs-lookup"><span data-stu-id="9c9da-131">-PackageAlias</span></span>
<span data-ttu-id="9c9da-132">[提取 MSIX] 影像的封裝別名</span><span class="sxs-lookup"><span data-stu-id="9c9da-132">Package Alias from extract MSIX Image</span></span>

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

### <span data-ttu-id="9c9da-133">-PackageApplication</span><span class="sxs-lookup"><span data-stu-id="9c9da-133">-PackageApplication</span></span>
<span data-ttu-id="9c9da-134">套件應用程式清單。</span><span class="sxs-lookup"><span data-stu-id="9c9da-134">List of package applications.</span></span>

<span data-ttu-id="9c9da-135">若要建立，請參閱 PACKAGEAPPLICATION 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="9c9da-135">To construct, see NOTES section for PACKAGEAPPLICATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackageApplications[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c9da-136">-PackageDependency</span><span class="sxs-lookup"><span data-stu-id="9c9da-136">-PackageDependency</span></span>
<span data-ttu-id="9c9da-137">套件相依性清單。</span><span class="sxs-lookup"><span data-stu-id="9c9da-137">List of package dependencies.</span></span>

<span data-ttu-id="9c9da-138">若要建立，請參閱 PACKAGEDEPENDENCY 屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="9c9da-138">To construct, see NOTES section for PACKAGEDEPENDENCY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackageDependencies[]
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c9da-139">-PackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="9c9da-139">-PackageFamilyName</span></span>
<span data-ttu-id="9c9da-140">從 appxmanifest.xml 封裝系列名稱。</span><span class="sxs-lookup"><span data-stu-id="9c9da-140">Package Family Name from appxmanifest.xml.</span></span>
<span data-ttu-id="9c9da-141">包含套件名稱和發行者名稱。</span><span class="sxs-lookup"><span data-stu-id="9c9da-141">Contains Package Name and Publisher name.</span></span>

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

### <span data-ttu-id="9c9da-142">-PackageName</span><span class="sxs-lookup"><span data-stu-id="9c9da-142">-PackageName</span></span>
<span data-ttu-id="9c9da-143">appxmanifest.xml 的套件名稱。</span><span class="sxs-lookup"><span data-stu-id="9c9da-143">Package Name from appxmanifest.xml.</span></span>

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

### <span data-ttu-id="9c9da-144">-PackageRelativePath</span><span class="sxs-lookup"><span data-stu-id="9c9da-144">-PackageRelativePath</span></span>
<span data-ttu-id="9c9da-145">影像內之套件的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="9c9da-145">Relative Path to the package inside the image.</span></span>

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

### <span data-ttu-id="9c9da-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c9da-146">-ResourceGroupName</span></span>
<span data-ttu-id="9c9da-147">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c9da-147">The name of the resource group.</span></span>
<span data-ttu-id="9c9da-148">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="9c9da-148">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9c9da-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c9da-149">-SubscriptionId</span></span>
<span data-ttu-id="9c9da-150">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="9c9da-150">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9c9da-151">-版本</span><span class="sxs-lookup"><span data-stu-id="9c9da-151">-Version</span></span>
<span data-ttu-id="9c9da-152">在 appxmanifest.xml 中找到套件版本。</span><span class="sxs-lookup"><span data-stu-id="9c9da-152">Package Version found in the appxmanifest.xml.</span></span>

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

### <span data-ttu-id="9c9da-153">-確認</span><span class="sxs-lookup"><span data-stu-id="9c9da-153">-Confirm</span></span>
<span data-ttu-id="9c9da-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9c9da-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c9da-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c9da-155">-WhatIf</span></span>
<span data-ttu-id="9c9da-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9c9da-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c9da-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9c9da-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c9da-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c9da-158">CommonParameters</span></span>
<span data-ttu-id="9c9da-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9c9da-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c9da-160">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9c9da-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c9da-161">輸入</span><span class="sxs-lookup"><span data-stu-id="9c9da-161">INPUTS</span></span>

## <span data-ttu-id="9c9da-162">輸出</span><span class="sxs-lookup"><span data-stu-id="9c9da-162">OUTPUTS</span></span>

### <span data-ttu-id="9c9da-163">IMsixPackage （DesktopVirtualization）。 Api20201019Preview。</span><span class="sxs-lookup"><span data-stu-id="9c9da-163">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixPackage</span></span>

## <span data-ttu-id="9c9da-164">筆記</span><span class="sxs-lookup"><span data-stu-id="9c9da-164">NOTES</span></span>

<span data-ttu-id="9c9da-165">別名</span><span class="sxs-lookup"><span data-stu-id="9c9da-165">ALIASES</span></span>

<span data-ttu-id="9c9da-166">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="9c9da-166">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9c9da-167">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="9c9da-167">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9c9da-168">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="9c9da-168">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9c9da-169">PACKAGEAPPLICATION <IMsixPackageApplications [] >：套件應用程式清單。</span><span class="sxs-lookup"><span data-stu-id="9c9da-169">PACKAGEAPPLICATION <IMsixPackageApplications[]>: List of package applications.</span></span> 
  - <span data-ttu-id="9c9da-170">`[AppId <String>]`：封裝應用程式識別碼，在 appxmanifest.xml 中找到。</span><span class="sxs-lookup"><span data-stu-id="9c9da-170">`[AppId <String>]`: Package Application Id, found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="9c9da-171">`[AppUserModelId <String>]`：用於啟動封裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="9c9da-171">`[AppUserModelId <String>]`: Used to activate Package Application.</span></span> <span data-ttu-id="9c9da-172">由套件名稱和 ApplicationID 組成。</span><span class="sxs-lookup"><span data-stu-id="9c9da-172">Consists of Package Name and ApplicationID.</span></span> <span data-ttu-id="9c9da-173">在 appxmanifest.xml 中找到。</span><span class="sxs-lookup"><span data-stu-id="9c9da-173">Found in appxmanifest.xml.</span></span>
  - <span data-ttu-id="9c9da-174">`[Description <String>]`：封裝應用程式的描述。</span><span class="sxs-lookup"><span data-stu-id="9c9da-174">`[Description <String>]`: Description of Package Application.</span></span>
  - <span data-ttu-id="9c9da-175">`[FriendlyName <String>]`：使用者的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="9c9da-175">`[FriendlyName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="9c9da-176">`[IconImageName <String>]`：使用者的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="9c9da-176">`[IconImageName <String>]`: User friendly name.</span></span>
  - <span data-ttu-id="9c9da-177">`[RawIcon <Byte[]>]`：圖示 a 64 位字串做為位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="9c9da-177">`[RawIcon <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>
  - <span data-ttu-id="9c9da-178">`[RawPng <Byte[]>]`：圖示 a 64 位字串做為位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="9c9da-178">`[RawPng <Byte[]>]`: the icon a 64 bit string as a byte array.</span></span>

<span data-ttu-id="9c9da-179">PACKAGEDEPENDENCY <IMsixPackageDependencies [] >：套件相依性清單。</span><span class="sxs-lookup"><span data-stu-id="9c9da-179">PACKAGEDEPENDENCY <IMsixPackageDependencies[]>: List of package dependencies.</span></span> 
  - <span data-ttu-id="9c9da-180">`[DependencyName <String>]`：套件相依性的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c9da-180">`[DependencyName <String>]`: Name of package dependency.</span></span>
  - <span data-ttu-id="9c9da-181">`[MinVersion <String>]`：需要相依性版本。</span><span class="sxs-lookup"><span data-stu-id="9c9da-181">`[MinVersion <String>]`: Dependency version required.</span></span>
  - <span data-ttu-id="9c9da-182">`[Publisher <String>]`：相依性發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="9c9da-182">`[Publisher <String>]`: Name of dependency publisher.</span></span>

## <span data-ttu-id="9c9da-183">相關連結</span><span class="sxs-lookup"><span data-stu-id="9c9da-183">RELATED LINKS</span></span>

