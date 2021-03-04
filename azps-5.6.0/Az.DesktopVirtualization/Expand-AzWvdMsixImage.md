---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/expand-azwvdmsiximage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
ms.openlocfilehash: f4767b87e7230727a2cf9c83af0c2aa5d03b908a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905470"
---
# <span data-ttu-id="8d8d1-101">Expand-AzWvdMsixImage</span><span class="sxs-lookup"><span data-stu-id="8d8d1-101">Expand-AzWvdMsixImage</span></span>

## <span data-ttu-id="8d8d1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8d8d1-102">SYNOPSIS</span></span>
<span data-ttu-id="8d8d1-103">展開並列出圖像中的 MSIX 套件 ，並給予圖像路徑。</span><span class="sxs-lookup"><span data-stu-id="8d8d1-103">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="8d8d1-104">語法</span><span class="sxs-lookup"><span data-stu-id="8d8d1-104">SYNTAX</span></span>

### <span data-ttu-id="8d8d1-105">ExpandExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="8d8d1-105">ExpandExpanded (Default)</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Uri <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8d8d1-106">擴大</span><span class="sxs-lookup"><span data-stu-id="8d8d1-106">Expand</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> -MsixImageUri <IMsixImageUri>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8d8d1-107">ExpandViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8d8d1-107">ExpandViaIdentity</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> -MsixImageUri <IMsixImageUri>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8d8d1-108">ExpandViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8d8d1-108">ExpandViaIdentityExpanded</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> [-Uri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8d8d1-109">描述</span><span class="sxs-lookup"><span data-stu-id="8d8d1-109">DESCRIPTION</span></span>
<span data-ttu-id="8d8d1-110">展開並列出圖像中的 MSIX 套件 ，並給予圖像路徑。</span><span class="sxs-lookup"><span data-stu-id="8d8d1-110">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="8d8d1-111">例子</span><span class="sxs-lookup"><span data-stu-id="8d8d1-111">EXAMPLES</span></span>

### <span data-ttu-id="8d8d1-112">範例 1：展開指定的圖像路徑，並取回在圖像中找到的套件中繼資料AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="8d8d1-112">Example 1: Expands specified Image Path and retrieves Package metadata found in AppxManifest.xml</span></span>
```powershell
PS C:\> Expand-AzWvdMsixImage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
          -Uri ImagePathURI

Name                          Type
----                          ----
HostPoolName/extractmsiximage Microsoft.DesktopVirtualization/hostpools/extractmsiximage
```

<span data-ttu-id="8d8d1-113">此命令會返回在給定圖像路徑中找到的 MSIX 套件中繼資料。</span><span class="sxs-lookup"><span data-stu-id="8d8d1-113">This command returns Metadata of MSIX Package found in the given Image Path.</span></span>

## <span data-ttu-id="8d8d1-114">參數</span><span class="sxs-lookup"><span data-stu-id="8d8d1-114">PARAMETERS</span></span>

### <span data-ttu-id="8d8d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d8d1-115">-DefaultProfile</span></span>
<span data-ttu-id="8d8d1-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8d8d1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d8d1-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="8d8d1-117">-HostPoolName</span></span>
<span data-ttu-id="8d8d1-118">指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="8d8d1-118">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d8d1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d8d1-119">-InputObject</span></span>
<span data-ttu-id="8d8d1-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8d8d1-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: ExpandViaIdentity, ExpandViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d8d1-121">-MsixImageUri</span><span class="sxs-lookup"><span data-stu-id="8d8d1-121">-MsixImageUri</span></span>
<span data-ttu-id="8d8d1-122">代表參照 MSIX 圖像至建構的 URI，請參閱 MSIXIMAGEURI 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8d8d1-122">Represents URI referring to MSIX Image To construct, see NOTES section for MSIXIMAGEURI properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri
Parameter Sets: Expand, ExpandViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d8d1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d8d1-123">-ResourceGroupName</span></span>
<span data-ttu-id="8d8d1-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d8d1-124">The name of the resource group.</span></span>
<span data-ttu-id="8d8d1-125">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="8d8d1-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d8d1-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d8d1-126">-SubscriptionId</span></span>
<span data-ttu-id="8d8d1-127">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8d8d1-127">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Expand, ExpandExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d8d1-128">-Uri</span><span class="sxs-lookup"><span data-stu-id="8d8d1-128">-Uri</span></span>
<span data-ttu-id="8d8d1-129">URI 對圖像</span><span class="sxs-lookup"><span data-stu-id="8d8d1-129">URI to Image</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandExpanded, ExpandViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d8d1-130">-確認</span><span class="sxs-lookup"><span data-stu-id="8d8d1-130">-Confirm</span></span>
<span data-ttu-id="8d8d1-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8d8d1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d8d1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d8d1-132">-WhatIf</span></span>
<span data-ttu-id="8d8d1-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8d8d1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d8d1-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8d8d1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d8d1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d8d1-135">CommonParameters</span></span>
<span data-ttu-id="8d8d1-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8d8d1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d8d1-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d8d1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d8d1-138">輸入</span><span class="sxs-lookup"><span data-stu-id="8d8d1-138">INPUTS</span></span>

### <span data-ttu-id="8d8d1-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.Api20201102Preview.IMsixImageUri</span><span class="sxs-lookup"><span data-stu-id="8d8d1-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IMsixImageUri</span></span>

### <span data-ttu-id="8d8d1-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="8d8d1-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="8d8d1-141">輸出</span><span class="sxs-lookup"><span data-stu-id="8d8d1-141">OUTPUTS</span></span>

### <span data-ttu-id="8d8d1-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.Api20201102Preview.IExpandMsixImage</span><span class="sxs-lookup"><span data-stu-id="8d8d1-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IExpandMsixImage</span></span>

## <span data-ttu-id="8d8d1-143">筆記</span><span class="sxs-lookup"><span data-stu-id="8d8d1-143">NOTES</span></span>

<span data-ttu-id="8d8d1-144">別名</span><span class="sxs-lookup"><span data-stu-id="8d8d1-144">ALIASES</span></span>

<span data-ttu-id="8d8d1-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8d8d1-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8d8d1-146">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8d8d1-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8d8d1-147">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8d8d1-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8d8d1-148">INPUTOBJECT： <IDesktopVirtualizationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="8d8d1-148">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8d8d1-149">`[ApplicationGroupName <String>]`：應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="8d8d1-149">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="8d8d1-150">`[ApplicationName <String>]`：指定應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="8d8d1-150">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="8d8d1-151">`[DesktopName <String>]`：指定桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="8d8d1-151">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="8d8d1-152">`[HostPoolName <String>]`：指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="8d8d1-152">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="8d8d1-153">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="8d8d1-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8d8d1-154">`[MsixPackageFullName <String>]`：指定主機多工緩衝處理程式中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="8d8d1-154">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="8d8d1-155">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8d8d1-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8d8d1-156">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="8d8d1-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="8d8d1-157">`[SessionHostName <String>]`：指定主機集中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="8d8d1-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="8d8d1-158">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8d8d1-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8d8d1-159">`[UserSessionId <String>]`：指定工作階段主機內的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="8d8d1-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="8d8d1-160">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="8d8d1-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

<span data-ttu-id="8d8d1-161">MSIXIMAGEURI： <IMsixImageUri> 代表參照 MSIX 圖像的 URI</span><span class="sxs-lookup"><span data-stu-id="8d8d1-161">MSIXIMAGEURI <IMsixImageUri>: Represents URI referring to MSIX Image</span></span>
  - <span data-ttu-id="8d8d1-162">`[Uri <String>]`：URI 對圖像</span><span class="sxs-lookup"><span data-stu-id="8d8d1-162">`[Uri <String>]`: URI to Image</span></span>

## <span data-ttu-id="8d8d1-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="8d8d1-163">RELATED LINKS</span></span>

