---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
ms.openlocfilehash: da00f15a43b74cbdbc516b86da442f0777775627
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284734"
---
# <span data-ttu-id="25bcb-101">Remove-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="25bcb-101">Remove-AzWvdUserSession</span></span>

## <span data-ttu-id="25bcb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="25bcb-102">SYNOPSIS</span></span>
<span data-ttu-id="25bcb-103">移除 userSession。</span><span class="sxs-lookup"><span data-stu-id="25bcb-103">Remove a userSession.</span></span>

## <span data-ttu-id="25bcb-104">句法</span><span class="sxs-lookup"><span data-stu-id="25bcb-104">SYNTAX</span></span>

### <span data-ttu-id="25bcb-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="25bcb-105">Delete (Default)</span></span>
```
Remove-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="25bcb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="25bcb-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="25bcb-107">說明</span><span class="sxs-lookup"><span data-stu-id="25bcb-107">DESCRIPTION</span></span>
<span data-ttu-id="25bcb-108">移除 userSession。</span><span class="sxs-lookup"><span data-stu-id="25bcb-108">Remove a userSession.</span></span>

## <span data-ttu-id="25bcb-109">示例</span><span class="sxs-lookup"><span data-stu-id="25bcb-109">EXAMPLES</span></span>

### <span data-ttu-id="25bcb-110">範例1：依名稱刪除 Windows 虛擬桌面 UserSession</span><span class="sxs-lookup"><span data-stu-id="25bcb-110">Example 1: Delete a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Remove-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="25bcb-111">這個命令會刪除工作階段主機中的 Windows 虛擬桌面 UserSession。</span><span class="sxs-lookup"><span data-stu-id="25bcb-111">This command deletes a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="25bcb-112">參數</span><span class="sxs-lookup"><span data-stu-id="25bcb-112">PARAMETERS</span></span>

### <span data-ttu-id="25bcb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25bcb-113">-DefaultProfile</span></span>
<span data-ttu-id="25bcb-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="25bcb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25bcb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="25bcb-115">-Force</span></span>
<span data-ttu-id="25bcb-116">[強制] 標記以 userSession 登入。</span><span class="sxs-lookup"><span data-stu-id="25bcb-116">Force flag to login off userSession.</span></span>

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

### <span data-ttu-id="25bcb-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="25bcb-117">-HostPoolName</span></span>
<span data-ttu-id="25bcb-118">指定資源群組中主機池的名稱</span><span class="sxs-lookup"><span data-stu-id="25bcb-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="25bcb-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="25bcb-119">-Id</span></span>
<span data-ttu-id="25bcb-120">指定的工作階段主機中使用者會話的名稱</span><span class="sxs-lookup"><span data-stu-id="25bcb-120">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25bcb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25bcb-121">-InputObject</span></span>
<span data-ttu-id="25bcb-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="25bcb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="25bcb-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25bcb-123">-PassThru</span></span>
<span data-ttu-id="25bcb-124">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="25bcb-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="25bcb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25bcb-125">-ResourceGroupName</span></span>
<span data-ttu-id="25bcb-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="25bcb-126">The name of the resource group.</span></span>
<span data-ttu-id="25bcb-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="25bcb-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="25bcb-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="25bcb-128">-SessionHostName</span></span>
<span data-ttu-id="25bcb-129">指定主機池中工作階段主機的名稱</span><span class="sxs-lookup"><span data-stu-id="25bcb-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="25bcb-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25bcb-130">-SubscriptionId</span></span>
<span data-ttu-id="25bcb-131">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="25bcb-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="25bcb-132">-確認</span><span class="sxs-lookup"><span data-stu-id="25bcb-132">-Confirm</span></span>
<span data-ttu-id="25bcb-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="25bcb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25bcb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25bcb-134">-WhatIf</span></span>
<span data-ttu-id="25bcb-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="25bcb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25bcb-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="25bcb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25bcb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25bcb-137">CommonParameters</span></span>
<span data-ttu-id="25bcb-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="25bcb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25bcb-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="25bcb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25bcb-140">輸入</span><span class="sxs-lookup"><span data-stu-id="25bcb-140">INPUTS</span></span>

### <span data-ttu-id="25bcb-141">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="25bcb-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="25bcb-142">輸出</span><span class="sxs-lookup"><span data-stu-id="25bcb-142">OUTPUTS</span></span>

### <span data-ttu-id="25bcb-143">System.object</span><span class="sxs-lookup"><span data-stu-id="25bcb-143">System.Boolean</span></span>

## <span data-ttu-id="25bcb-144">筆記</span><span class="sxs-lookup"><span data-stu-id="25bcb-144">NOTES</span></span>

<span data-ttu-id="25bcb-145">別名</span><span class="sxs-lookup"><span data-stu-id="25bcb-145">ALIASES</span></span>

<span data-ttu-id="25bcb-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="25bcb-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="25bcb-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="25bcb-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="25bcb-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="25bcb-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="25bcb-149">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="25bcb-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="25bcb-150">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="25bcb-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="25bcb-151">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="25bcb-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="25bcb-152">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="25bcb-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="25bcb-153">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="25bcb-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="25bcb-154">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="25bcb-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="25bcb-155">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="25bcb-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="25bcb-156">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="25bcb-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="25bcb-157">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="25bcb-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="25bcb-158">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="25bcb-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="25bcb-159">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="25bcb-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="25bcb-160">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="25bcb-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="25bcb-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="25bcb-161">RELATED LINKS</span></span>

