---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdWorkspace.md
ms.openlocfilehash: 04e7c192659ec1f1aa71b0bf1b97e61030cd9b4e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274900"
---
# <span data-ttu-id="4f7aa-101">Update-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="4f7aa-101">Update-AzWvdWorkspace</span></span>

## <span data-ttu-id="4f7aa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f7aa-102">SYNOPSIS</span></span>
<span data-ttu-id="4f7aa-103">更新工作區。</span><span class="sxs-lookup"><span data-stu-id="4f7aa-103">Update a workspace.</span></span>

## <span data-ttu-id="4f7aa-104">句法</span><span class="sxs-lookup"><span data-stu-id="4f7aa-104">SYNTAX</span></span>

### <span data-ttu-id="4f7aa-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="4f7aa-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ApplicationGroupReference <String[]>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4f7aa-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4f7aa-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-ApplicationGroupReference <String[]>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4f7aa-107">說明</span><span class="sxs-lookup"><span data-stu-id="4f7aa-107">DESCRIPTION</span></span>
<span data-ttu-id="4f7aa-108">更新工作區。</span><span class="sxs-lookup"><span data-stu-id="4f7aa-108">Update a workspace.</span></span>

## <span data-ttu-id="4f7aa-109">示例</span><span class="sxs-lookup"><span data-stu-id="4f7aa-109">EXAMPLES</span></span>

### <span data-ttu-id="4f7aa-110">範例1：依名稱更新 Windows 虛擬桌面工作區</span><span class="sxs-lookup"><span data-stu-id="4f7aa-110">Example 1: Update a Windows Virtual Desktop Workspace by name</span></span>
```powershell
PS C:\> Update-AzWvdWorkspace -ResourceGroupName ResourceGroupName `
                        -Name WorkspaceName `
                        -FriendlyName 'Friendly Name' `
                        -ApplicationGroupReference "/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName1","/subscriptions/SubscriptionId/resourceGroups/ResourceGroupName/providers/Microsoft.DesktopVirtualization/applicationGroups/ApplicationGroupName2" `
                        -Description 'Description'

Location   Name                 Type
--------   ----                 ----
eastus     WorkspaceName Microsoft.DesktopVirtualization/workspaces
```

<span data-ttu-id="4f7aa-111">這個命令會更新資源群組中的 Windows 虛擬桌面工作區。</span><span class="sxs-lookup"><span data-stu-id="4f7aa-111">This command updates a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="4f7aa-112">參數</span><span class="sxs-lookup"><span data-stu-id="4f7aa-112">PARAMETERS</span></span>

### <span data-ttu-id="4f7aa-113">-ApplicationGroupReference</span><span class="sxs-lookup"><span data-stu-id="4f7aa-113">-ApplicationGroupReference</span></span>
<span data-ttu-id="4f7aa-114">ApplicationGroup 連結清單。</span><span class="sxs-lookup"><span data-stu-id="4f7aa-114">List of applicationGroup links.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f7aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f7aa-115">-DefaultProfile</span></span>
<span data-ttu-id="4f7aa-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f7aa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f7aa-117">-描述</span><span class="sxs-lookup"><span data-stu-id="4f7aa-117">-Description</span></span>
<span data-ttu-id="4f7aa-118">工作區的描述。</span><span class="sxs-lookup"><span data-stu-id="4f7aa-118">Description of Workspace.</span></span>

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

### <span data-ttu-id="4f7aa-119">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4f7aa-119">-FriendlyName</span></span>
<span data-ttu-id="4f7aa-120">工作區的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="4f7aa-120">Friendly name of Workspace.</span></span>

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

### <span data-ttu-id="4f7aa-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f7aa-121">-InputObject</span></span>
<span data-ttu-id="4f7aa-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4f7aa-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f7aa-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="4f7aa-123">-Name</span></span>
<span data-ttu-id="4f7aa-124">工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="4f7aa-124">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f7aa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f7aa-125">-ResourceGroupName</span></span>
<span data-ttu-id="4f7aa-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f7aa-126">The name of the resource group.</span></span>
<span data-ttu-id="4f7aa-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="4f7aa-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f7aa-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4f7aa-128">-SubscriptionId</span></span>
<span data-ttu-id="4f7aa-129">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="4f7aa-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f7aa-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="4f7aa-130">-Tag</span></span>
<span data-ttu-id="4f7aa-131">要更新的標記</span><span class="sxs-lookup"><span data-stu-id="4f7aa-131">tags to be updated</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f7aa-132">-確認</span><span class="sxs-lookup"><span data-stu-id="4f7aa-132">-Confirm</span></span>
<span data-ttu-id="4f7aa-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4f7aa-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f7aa-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f7aa-134">-WhatIf</span></span>
<span data-ttu-id="4f7aa-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4f7aa-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f7aa-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4f7aa-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f7aa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f7aa-137">CommonParameters</span></span>
<span data-ttu-id="4f7aa-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f7aa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f7aa-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4f7aa-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f7aa-140">輸入</span><span class="sxs-lookup"><span data-stu-id="4f7aa-140">INPUTS</span></span>

### <span data-ttu-id="4f7aa-141">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="4f7aa-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="4f7aa-142">輸出</span><span class="sxs-lookup"><span data-stu-id="4f7aa-142">OUTPUTS</span></span>

### <span data-ttu-id="4f7aa-143">IWorkspace （DesktopVirtualization）。 Api20201019Preview。</span><span class="sxs-lookup"><span data-stu-id="4f7aa-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IWorkspace</span></span>

## <span data-ttu-id="4f7aa-144">筆記</span><span class="sxs-lookup"><span data-stu-id="4f7aa-144">NOTES</span></span>

<span data-ttu-id="4f7aa-145">別名</span><span class="sxs-lookup"><span data-stu-id="4f7aa-145">ALIASES</span></span>

<span data-ttu-id="4f7aa-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="4f7aa-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4f7aa-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="4f7aa-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4f7aa-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="4f7aa-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4f7aa-149">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="4f7aa-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4f7aa-150">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="4f7aa-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="4f7aa-151">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="4f7aa-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="4f7aa-152">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="4f7aa-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="4f7aa-153">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="4f7aa-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="4f7aa-154">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="4f7aa-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4f7aa-155">`[MsixPackageFullName <String>]`： MSIX 套件在指定 hostpool 中的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="4f7aa-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="4f7aa-156">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f7aa-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4f7aa-157">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="4f7aa-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="4f7aa-158">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="4f7aa-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="4f7aa-159">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4f7aa-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4f7aa-160">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="4f7aa-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="4f7aa-161">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="4f7aa-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="4f7aa-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f7aa-162">RELATED LINKS</span></span>

