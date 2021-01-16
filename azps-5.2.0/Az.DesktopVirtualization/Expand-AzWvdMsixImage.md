---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/expand-azwvdmsiximage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Expand-AzWvdMsixImage.md
ms.openlocfilehash: 417acf03af2bf73d57759841bacc3ed532e8f043
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279885"
---
# <span data-ttu-id="d3b70-101">Expand-AzWvdMsixImage</span><span class="sxs-lookup"><span data-stu-id="d3b70-101">Expand-AzWvdMsixImage</span></span>

## <span data-ttu-id="d3b70-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d3b70-102">SYNOPSIS</span></span>
<span data-ttu-id="d3b70-103">在已知影像路徑的情況下，展開並列出影像中的 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="d3b70-103">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="d3b70-104">句法</span><span class="sxs-lookup"><span data-stu-id="d3b70-104">SYNTAX</span></span>

### <span data-ttu-id="d3b70-105">ExpandExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="d3b70-105">ExpandExpanded (Default)</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Uri <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d3b70-106">擴充</span><span class="sxs-lookup"><span data-stu-id="d3b70-106">Expand</span></span>
```
Expand-AzWvdMsixImage -HostPoolName <String> -ResourceGroupName <String> -MsixImageUri <IMsixImageUri>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d3b70-107">ExpandViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d3b70-107">ExpandViaIdentity</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> -MsixImageUri <IMsixImageUri>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d3b70-108">ExpandViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d3b70-108">ExpandViaIdentityExpanded</span></span>
```
Expand-AzWvdMsixImage -InputObject <IDesktopVirtualizationIdentity> [-Uri <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d3b70-109">說明</span><span class="sxs-lookup"><span data-stu-id="d3b70-109">DESCRIPTION</span></span>
<span data-ttu-id="d3b70-110">在已知影像路徑的情況下，展開並列出影像中的 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="d3b70-110">Expands and Lists MSIX packages in an Image, given the Image Path.</span></span>

## <span data-ttu-id="d3b70-111">示例</span><span class="sxs-lookup"><span data-stu-id="d3b70-111">EXAMPLES</span></span>

### <span data-ttu-id="d3b70-112">範例1：展開指定的影像路徑，並檢索 AppxManifest.xml 中找到的套件中繼資料</span><span class="sxs-lookup"><span data-stu-id="d3b70-112">Example 1: Expands specified Image Path and retrieves Package metadata found in AppxManifest.xml</span></span>
```powershell
PS C:\> Expand-AzWvdMsixImage -HostPoolName HostPoolName `
          -ResourceGroupName resourceGroupName `
          -SubscriptionId SubscriptionId `
          -Uri ImagePathURI

Name                          Type
----                          ----
HostPoolName/extractmsiximage Microsoft.DesktopVirtualization/hostpools/extractmsiximage
```

<span data-ttu-id="d3b70-113">這個命令會傳回在指定的影像路徑中找到的 MSIX 套件中繼資料。</span><span class="sxs-lookup"><span data-stu-id="d3b70-113">This command returns Metadata of MSIX Package found in the given Image Path.</span></span>

## <span data-ttu-id="d3b70-114">參數</span><span class="sxs-lookup"><span data-stu-id="d3b70-114">PARAMETERS</span></span>

### <span data-ttu-id="d3b70-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3b70-115">-DefaultProfile</span></span>
<span data-ttu-id="d3b70-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d3b70-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3b70-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="d3b70-117">-HostPoolName</span></span>
<span data-ttu-id="d3b70-118">指定資源群組中主機池的名稱</span><span class="sxs-lookup"><span data-stu-id="d3b70-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="d3b70-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3b70-119">-InputObject</span></span>
<span data-ttu-id="d3b70-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d3b70-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d3b70-121">-MsixImageUri</span><span class="sxs-lookup"><span data-stu-id="d3b70-121">-MsixImageUri</span></span>
<span data-ttu-id="d3b70-122">代表 URI 以參照要構造的 MSIX 影像，請參閱 MSIXIMAGEURI 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d3b70-122">Represents URI referring to MSIX Image To construct, see NOTES section for MSIXIMAGEURI properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixImageUri
Parameter Sets: Expand, ExpandViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3b70-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3b70-123">-ResourceGroupName</span></span>
<span data-ttu-id="d3b70-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3b70-124">The name of the resource group.</span></span>
<span data-ttu-id="d3b70-125">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d3b70-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d3b70-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d3b70-126">-SubscriptionId</span></span>
<span data-ttu-id="d3b70-127">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="d3b70-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d3b70-128">-Uri</span><span class="sxs-lookup"><span data-stu-id="d3b70-128">-Uri</span></span>
<span data-ttu-id="d3b70-129">圖像的 URI</span><span class="sxs-lookup"><span data-stu-id="d3b70-129">URI to Image</span></span>

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

### <span data-ttu-id="d3b70-130">-確認</span><span class="sxs-lookup"><span data-stu-id="d3b70-130">-Confirm</span></span>
<span data-ttu-id="d3b70-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d3b70-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3b70-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3b70-132">-WhatIf</span></span>
<span data-ttu-id="d3b70-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d3b70-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3b70-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d3b70-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3b70-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3b70-135">CommonParameters</span></span>
<span data-ttu-id="d3b70-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d3b70-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3b70-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d3b70-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3b70-138">輸入</span><span class="sxs-lookup"><span data-stu-id="d3b70-138">INPUTS</span></span>

### <span data-ttu-id="d3b70-139">IMsixImageUri （DesktopVirtualization）。 Api20201019Preview。</span><span class="sxs-lookup"><span data-stu-id="d3b70-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IMsixImageUri</span></span>

### <span data-ttu-id="d3b70-140">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="d3b70-140">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="d3b70-141">輸出</span><span class="sxs-lookup"><span data-stu-id="d3b70-141">OUTPUTS</span></span>

### <span data-ttu-id="d3b70-142">IExpandMsixImage （DesktopVirtualization）。 Api20201019Preview。</span><span class="sxs-lookup"><span data-stu-id="d3b70-142">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IExpandMsixImage</span></span>

## <span data-ttu-id="d3b70-143">筆記</span><span class="sxs-lookup"><span data-stu-id="d3b70-143">NOTES</span></span>

<span data-ttu-id="d3b70-144">別名</span><span class="sxs-lookup"><span data-stu-id="d3b70-144">ALIASES</span></span>

<span data-ttu-id="d3b70-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="d3b70-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d3b70-146">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="d3b70-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d3b70-147">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="d3b70-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d3b70-148">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="d3b70-148">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d3b70-149">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="d3b70-149">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="d3b70-150">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="d3b70-150">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="d3b70-151">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="d3b70-151">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="d3b70-152">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="d3b70-152">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="d3b70-153">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="d3b70-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d3b70-154">`[MsixPackageFullName <String>]`： MSIX 套件在指定 hostpool 中的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="d3b70-154">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="d3b70-155">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3b70-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d3b70-156">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="d3b70-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="d3b70-157">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="d3b70-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="d3b70-158">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d3b70-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d3b70-159">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="d3b70-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="d3b70-160">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="d3b70-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

<span data-ttu-id="d3b70-161">MSIXIMAGEURI <IMsixImageUri> ：代表參照 MSIX 影像的 URI</span><span class="sxs-lookup"><span data-stu-id="d3b70-161">MSIXIMAGEURI <IMsixImageUri>: Represents URI referring to MSIX Image</span></span>
  - <span data-ttu-id="d3b70-162">`[Uri <String>]`： URI 至影像</span><span class="sxs-lookup"><span data-stu-id="d3b70-162">`[Uri <String>]`: URI to Image</span></span>

## <span data-ttu-id="d3b70-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="d3b70-163">RELATED LINKS</span></span>

