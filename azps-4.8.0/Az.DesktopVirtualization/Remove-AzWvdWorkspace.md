---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdWorkspace.md
ms.openlocfilehash: 420a73dc1890db1b26cff5ca5289dc030666b038
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128200"
---
# <span data-ttu-id="ab1a5-101">Remove-AzWvdWorkspace</span><span class="sxs-lookup"><span data-stu-id="ab1a5-101">Remove-AzWvdWorkspace</span></span>

## <span data-ttu-id="ab1a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab1a5-102">SYNOPSIS</span></span>
<span data-ttu-id="ab1a5-103">移除工作區。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-103">Remove a workspace.</span></span>

## <span data-ttu-id="ab1a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab1a5-104">SYNTAX</span></span>

### <span data-ttu-id="ab1a5-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="ab1a5-105">Delete (Default)</span></span>
```
Remove-AzWvdWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ab1a5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ab1a5-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdWorkspace -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ab1a5-107">說明</span><span class="sxs-lookup"><span data-stu-id="ab1a5-107">DESCRIPTION</span></span>
<span data-ttu-id="ab1a5-108">移除工作區。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-108">Remove a workspace.</span></span>

## <span data-ttu-id="ab1a5-109">示例</span><span class="sxs-lookup"><span data-stu-id="ab1a5-109">EXAMPLES</span></span>

### <span data-ttu-id="ab1a5-110">範例1：依名稱刪除 Windows 虛擬桌面 Worksapce</span><span class="sxs-lookup"><span data-stu-id="ab1a5-110">Example 1: Delete a Windows Virtual Desktop Worksapce by name</span></span>
```powershell
PS C:\> Remove-AzWvdWorksapce -ResourceGroupName ResourceGroupName -Name WorkspaceName
```

<span data-ttu-id="ab1a5-111">這個命令會刪除資源群組中的 Windows 虛擬桌面工作區。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-111">This command deletes a Windows Virtual Desktop Workspace in a Resource Group.</span></span>

## <span data-ttu-id="ab1a5-112">參數</span><span class="sxs-lookup"><span data-stu-id="ab1a5-112">PARAMETERS</span></span>

### <span data-ttu-id="ab1a5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab1a5-113">-DefaultProfile</span></span>
<span data-ttu-id="ab1a5-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab1a5-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab1a5-115">-InputObject</span></span>
<span data-ttu-id="ab1a5-116">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab1a5-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ab1a5-117">-Name</span></span>
<span data-ttu-id="ab1a5-118">工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="ab1a5-118">The name of the workspace</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1a5-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab1a5-119">-PassThru</span></span>
<span data-ttu-id="ab1a5-120">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="ab1a5-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ab1a5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab1a5-121">-ResourceGroupName</span></span>
<span data-ttu-id="ab1a5-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-122">The name of the resource group.</span></span>
<span data-ttu-id="ab1a5-123">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1a5-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ab1a5-124">-SubscriptionId</span></span>
<span data-ttu-id="ab1a5-125">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1a5-126">-確認</span><span class="sxs-lookup"><span data-stu-id="ab1a5-126">-Confirm</span></span>
<span data-ttu-id="ab1a5-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab1a5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab1a5-128">-WhatIf</span></span>
<span data-ttu-id="ab1a5-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab1a5-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab1a5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab1a5-131">CommonParameters</span></span>
<span data-ttu-id="ab1a5-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab1a5-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab1a5-134">輸入</span><span class="sxs-lookup"><span data-stu-id="ab1a5-134">INPUTS</span></span>

### <span data-ttu-id="ab1a5-135">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="ab1a5-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="ab1a5-136">輸出</span><span class="sxs-lookup"><span data-stu-id="ab1a5-136">OUTPUTS</span></span>

### <span data-ttu-id="ab1a5-137">System.object</span><span class="sxs-lookup"><span data-stu-id="ab1a5-137">System.Boolean</span></span>

## <span data-ttu-id="ab1a5-138">筆記</span><span class="sxs-lookup"><span data-stu-id="ab1a5-138">NOTES</span></span>

<span data-ttu-id="ab1a5-139">別名</span><span class="sxs-lookup"><span data-stu-id="ab1a5-139">ALIASES</span></span>

<span data-ttu-id="ab1a5-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="ab1a5-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ab1a5-141">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ab1a5-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ab1a5-143">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="ab1a5-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ab1a5-144">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="ab1a5-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="ab1a5-145">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="ab1a5-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="ab1a5-146">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="ab1a5-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="ab1a5-147">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="ab1a5-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="ab1a5-148">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="ab1a5-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ab1a5-149">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ab1a5-150">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="ab1a5-151">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="ab1a5-151">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="ab1a5-152">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ab1a5-152">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ab1a5-153">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="ab1a5-153">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="ab1a5-154">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="ab1a5-154">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="ab1a5-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab1a5-155">RELATED LINKS</span></span>

