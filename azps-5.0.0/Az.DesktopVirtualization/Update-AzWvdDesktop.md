---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
ms.openlocfilehash: 7aec3e71e65c20810d8a17e8f7fa14df3c69f577
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138925"
---
# <span data-ttu-id="aa407-101">Update-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="aa407-101">Update-AzWvdDesktop</span></span>

## <span data-ttu-id="aa407-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aa407-102">SYNOPSIS</span></span>
<span data-ttu-id="aa407-103">更新桌面。</span><span class="sxs-lookup"><span data-stu-id="aa407-103">Update a desktop.</span></span>

## <span data-ttu-id="aa407-104">句法</span><span class="sxs-lookup"><span data-stu-id="aa407-104">SYNTAX</span></span>

### <span data-ttu-id="aa407-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="aa407-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aa407-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="aa407-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="aa407-107">說明</span><span class="sxs-lookup"><span data-stu-id="aa407-107">DESCRIPTION</span></span>
<span data-ttu-id="aa407-108">更新桌面。</span><span class="sxs-lookup"><span data-stu-id="aa407-108">Update a desktop.</span></span>

## <span data-ttu-id="aa407-109">示例</span><span class="sxs-lookup"><span data-stu-id="aa407-109">EXAMPLES</span></span>

### <span data-ttu-id="aa407-110">範例1：更新 Windows 虛擬桌面電腦版</span><span class="sxs-lookup"><span data-stu-id="aa407-110">Example 1: Update a Windows Virtual Desktop Desktop</span></span>
```powershell
PS C:\> Update-AzWvdDesktop -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name DesktopName `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `

Name                             Type
----                             ----
ApplicationGroupName/DesktopName Microsoft.DesktopVirtualization/applicationgroups/desktops
```

<span data-ttu-id="aa407-111">這個命令會更新 applicaton 群組中的 Windows 虛擬桌面電腦桌面。</span><span class="sxs-lookup"><span data-stu-id="aa407-111">This command updates a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

## <span data-ttu-id="aa407-112">參數</span><span class="sxs-lookup"><span data-stu-id="aa407-112">PARAMETERS</span></span>

### <span data-ttu-id="aa407-113">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="aa407-113">-ApplicationGroupName</span></span>
<span data-ttu-id="aa407-114">應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="aa407-114">The name of the application group</span></span>

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

### <span data-ttu-id="aa407-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa407-115">-DefaultProfile</span></span>
<span data-ttu-id="aa407-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aa407-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa407-117">-描述</span><span class="sxs-lookup"><span data-stu-id="aa407-117">-Description</span></span>
<span data-ttu-id="aa407-118">桌面的描述。</span><span class="sxs-lookup"><span data-stu-id="aa407-118">Description of Desktop.</span></span>

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

### <span data-ttu-id="aa407-119">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="aa407-119">-FriendlyName</span></span>
<span data-ttu-id="aa407-120">桌上出版的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="aa407-120">Friendly name of Desktop.</span></span>

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

### <span data-ttu-id="aa407-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa407-121">-InputObject</span></span>
<span data-ttu-id="aa407-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="aa407-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="aa407-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="aa407-123">-Name</span></span>
<span data-ttu-id="aa407-124">指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="aa407-124">The name of the desktop within the specified desktop group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DesktopName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa407-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa407-125">-ResourceGroupName</span></span>
<span data-ttu-id="aa407-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa407-126">The name of the resource group.</span></span>
<span data-ttu-id="aa407-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="aa407-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="aa407-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa407-128">-SubscriptionId</span></span>
<span data-ttu-id="aa407-129">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="aa407-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="aa407-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="aa407-130">-Tag</span></span>
<span data-ttu-id="aa407-131">要更新的標記</span><span class="sxs-lookup"><span data-stu-id="aa407-131">tags to be updated</span></span>

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

### <span data-ttu-id="aa407-132">-確認</span><span class="sxs-lookup"><span data-stu-id="aa407-132">-Confirm</span></span>
<span data-ttu-id="aa407-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="aa407-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa407-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa407-134">-WhatIf</span></span>
<span data-ttu-id="aa407-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aa407-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa407-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aa407-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa407-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa407-137">CommonParameters</span></span>
<span data-ttu-id="aa407-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aa407-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa407-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="aa407-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa407-140">輸入</span><span class="sxs-lookup"><span data-stu-id="aa407-140">INPUTS</span></span>

### <span data-ttu-id="aa407-141">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="aa407-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="aa407-142">輸出</span><span class="sxs-lookup"><span data-stu-id="aa407-142">OUTPUTS</span></span>

### <span data-ttu-id="aa407-143">IDesktop （DesktopVirtualization）。 Api20191210Preview。</span><span class="sxs-lookup"><span data-stu-id="aa407-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktop</span></span>

## <span data-ttu-id="aa407-144">筆記</span><span class="sxs-lookup"><span data-stu-id="aa407-144">NOTES</span></span>

<span data-ttu-id="aa407-145">別名</span><span class="sxs-lookup"><span data-stu-id="aa407-145">ALIASES</span></span>

<span data-ttu-id="aa407-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="aa407-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aa407-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="aa407-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aa407-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="aa407-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aa407-149">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="aa407-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aa407-150">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="aa407-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="aa407-151">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="aa407-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="aa407-152">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="aa407-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="aa407-153">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="aa407-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="aa407-154">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="aa407-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aa407-155">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa407-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="aa407-156">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="aa407-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="aa407-157">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="aa407-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="aa407-158">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="aa407-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="aa407-159">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="aa407-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="aa407-160">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="aa407-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="aa407-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="aa407-161">RELATED LINKS</span></span>

