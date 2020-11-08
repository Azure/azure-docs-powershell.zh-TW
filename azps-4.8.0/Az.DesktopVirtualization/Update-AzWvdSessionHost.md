---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdSessionHost.md
ms.openlocfilehash: ec80e3382c401f9d64fb469c58a074ed47719ee9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971104"
---
# <span data-ttu-id="57c88-101">Update-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="57c88-101">Update-AzWvdSessionHost</span></span>

## <span data-ttu-id="57c88-102">摘要</span><span class="sxs-lookup"><span data-stu-id="57c88-102">SYNOPSIS</span></span>
<span data-ttu-id="57c88-103">更新工作階段主機。</span><span class="sxs-lookup"><span data-stu-id="57c88-103">Update a session host.</span></span>

## <span data-ttu-id="57c88-104">句法</span><span class="sxs-lookup"><span data-stu-id="57c88-104">SYNTAX</span></span>

### <span data-ttu-id="57c88-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="57c88-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AllowNewSession] [-AssignedUser <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="57c88-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="57c88-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-AllowNewSession]
 [-AssignedUser <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="57c88-107">說明</span><span class="sxs-lookup"><span data-stu-id="57c88-107">DESCRIPTION</span></span>
<span data-ttu-id="57c88-108">更新工作階段主機。</span><span class="sxs-lookup"><span data-stu-id="57c88-108">Update a session host.</span></span>

## <span data-ttu-id="57c88-109">示例</span><span class="sxs-lookup"><span data-stu-id="57c88-109">EXAMPLES</span></span>

### <span data-ttu-id="57c88-110">範例1：依名稱更新 Windows 虛擬桌面 SessionHost</span><span class="sxs-lookup"><span data-stu-id="57c88-110">Example 1: Update a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Update-AzWvdSessionHost -ResourceGroupName ResourceGroupName `
                            -HostPoolName HostPoolName `
                            -Name SessionHostName `
                            -AllowNewSession:$false

Name                                               Type
----                                               ----
HostPoolName/SessionHostName Microsoft.DesktopVirtualization/hostpools/sessionhosts
```

<span data-ttu-id="57c88-111">這個命令會更新主機池中的 Windows 虛擬桌面 SessionHost。</span><span class="sxs-lookup"><span data-stu-id="57c88-111">This command updates a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="57c88-112">參數</span><span class="sxs-lookup"><span data-stu-id="57c88-112">PARAMETERS</span></span>

### <span data-ttu-id="57c88-113">-AllowNewSession</span><span class="sxs-lookup"><span data-stu-id="57c88-113">-AllowNewSession</span></span>
<span data-ttu-id="57c88-114">允許新的會話。</span><span class="sxs-lookup"><span data-stu-id="57c88-114">Allow a new session.</span></span>

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

### <span data-ttu-id="57c88-115">-AssignedUser</span><span class="sxs-lookup"><span data-stu-id="57c88-115">-AssignedUser</span></span>
<span data-ttu-id="57c88-116">指派給 SessionHost 的使用者。</span><span class="sxs-lookup"><span data-stu-id="57c88-116">User assigned to SessionHost.</span></span>

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

### <span data-ttu-id="57c88-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57c88-117">-DefaultProfile</span></span>
<span data-ttu-id="57c88-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="57c88-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57c88-119">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="57c88-119">-HostPoolName</span></span>
<span data-ttu-id="57c88-120">指定資源群組中主機池的名稱</span><span class="sxs-lookup"><span data-stu-id="57c88-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="57c88-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57c88-121">-InputObject</span></span>
<span data-ttu-id="57c88-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="57c88-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="57c88-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="57c88-123">-Name</span></span>
<span data-ttu-id="57c88-124">指定主機池中工作階段主機的名稱</span><span class="sxs-lookup"><span data-stu-id="57c88-124">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c88-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57c88-125">-ResourceGroupName</span></span>
<span data-ttu-id="57c88-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="57c88-126">The name of the resource group.</span></span>
<span data-ttu-id="57c88-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="57c88-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="57c88-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57c88-128">-SubscriptionId</span></span>
<span data-ttu-id="57c88-129">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="57c88-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="57c88-130">-確認</span><span class="sxs-lookup"><span data-stu-id="57c88-130">-Confirm</span></span>
<span data-ttu-id="57c88-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="57c88-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57c88-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57c88-132">-WhatIf</span></span>
<span data-ttu-id="57c88-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="57c88-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57c88-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57c88-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57c88-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57c88-135">CommonParameters</span></span>
<span data-ttu-id="57c88-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="57c88-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57c88-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="57c88-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57c88-138">輸入</span><span class="sxs-lookup"><span data-stu-id="57c88-138">INPUTS</span></span>

### <span data-ttu-id="57c88-139">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="57c88-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="57c88-140">輸出</span><span class="sxs-lookup"><span data-stu-id="57c88-140">OUTPUTS</span></span>

### <span data-ttu-id="57c88-141">ISessionHost （DesktopVirtualization）。 Api20191210Preview。</span><span class="sxs-lookup"><span data-stu-id="57c88-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.ISessionHost</span></span>

## <span data-ttu-id="57c88-142">筆記</span><span class="sxs-lookup"><span data-stu-id="57c88-142">NOTES</span></span>

<span data-ttu-id="57c88-143">別名</span><span class="sxs-lookup"><span data-stu-id="57c88-143">ALIASES</span></span>

<span data-ttu-id="57c88-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="57c88-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="57c88-145">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="57c88-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57c88-146">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="57c88-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="57c88-147">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="57c88-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="57c88-148">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="57c88-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="57c88-149">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="57c88-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="57c88-150">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="57c88-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="57c88-151">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="57c88-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="57c88-152">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="57c88-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="57c88-153">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="57c88-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="57c88-154">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="57c88-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="57c88-155">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="57c88-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="57c88-156">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="57c88-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="57c88-157">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="57c88-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="57c88-158">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="57c88-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="57c88-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="57c88-159">RELATED LINKS</span></span>

