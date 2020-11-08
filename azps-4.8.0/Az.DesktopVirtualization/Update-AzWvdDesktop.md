---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvddesktop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdDesktop.md
ms.openlocfilehash: 7aec3e71e65c20810d8a17e8f7fa14df3c69f577
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971103"
---
# <span data-ttu-id="68ebe-101">Update-AzWvdDesktop</span><span class="sxs-lookup"><span data-stu-id="68ebe-101">Update-AzWvdDesktop</span></span>

## <span data-ttu-id="68ebe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="68ebe-102">SYNOPSIS</span></span>
<span data-ttu-id="68ebe-103">更新桌面。</span><span class="sxs-lookup"><span data-stu-id="68ebe-103">Update a desktop.</span></span>

## <span data-ttu-id="68ebe-104">句法</span><span class="sxs-lookup"><span data-stu-id="68ebe-104">SYNTAX</span></span>

### <span data-ttu-id="68ebe-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="68ebe-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdDesktop -ApplicationGroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="68ebe-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="68ebe-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdDesktop -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="68ebe-107">說明</span><span class="sxs-lookup"><span data-stu-id="68ebe-107">DESCRIPTION</span></span>
<span data-ttu-id="68ebe-108">更新桌面。</span><span class="sxs-lookup"><span data-stu-id="68ebe-108">Update a desktop.</span></span>

## <span data-ttu-id="68ebe-109">示例</span><span class="sxs-lookup"><span data-stu-id="68ebe-109">EXAMPLES</span></span>

### <span data-ttu-id="68ebe-110">範例1：更新 Windows 虛擬桌面電腦版</span><span class="sxs-lookup"><span data-stu-id="68ebe-110">Example 1: Update a Windows Virtual Desktop Desktop</span></span>
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

<span data-ttu-id="68ebe-111">這個命令會更新 applicaton 群組中的 Windows 虛擬桌面電腦桌面。</span><span class="sxs-lookup"><span data-stu-id="68ebe-111">This command updates a Windows Virtual Desktop Desktop in an applicaton Group.</span></span>

## <span data-ttu-id="68ebe-112">參數</span><span class="sxs-lookup"><span data-stu-id="68ebe-112">PARAMETERS</span></span>

### <span data-ttu-id="68ebe-113">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="68ebe-113">-ApplicationGroupName</span></span>
<span data-ttu-id="68ebe-114">應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="68ebe-114">The name of the application group</span></span>

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

### <span data-ttu-id="68ebe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68ebe-115">-DefaultProfile</span></span>
<span data-ttu-id="68ebe-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="68ebe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68ebe-117">-描述</span><span class="sxs-lookup"><span data-stu-id="68ebe-117">-Description</span></span>
<span data-ttu-id="68ebe-118">桌面的描述。</span><span class="sxs-lookup"><span data-stu-id="68ebe-118">Description of Desktop.</span></span>

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

### <span data-ttu-id="68ebe-119">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="68ebe-119">-FriendlyName</span></span>
<span data-ttu-id="68ebe-120">桌上出版的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="68ebe-120">Friendly name of Desktop.</span></span>

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

### <span data-ttu-id="68ebe-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="68ebe-121">-InputObject</span></span>
<span data-ttu-id="68ebe-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="68ebe-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="68ebe-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="68ebe-123">-Name</span></span>
<span data-ttu-id="68ebe-124">指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="68ebe-124">The name of the desktop within the specified desktop group</span></span>

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

### <span data-ttu-id="68ebe-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68ebe-125">-ResourceGroupName</span></span>
<span data-ttu-id="68ebe-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="68ebe-126">The name of the resource group.</span></span>
<span data-ttu-id="68ebe-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="68ebe-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="68ebe-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="68ebe-128">-SubscriptionId</span></span>
<span data-ttu-id="68ebe-129">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="68ebe-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="68ebe-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="68ebe-130">-Tag</span></span>
<span data-ttu-id="68ebe-131">要更新的標記</span><span class="sxs-lookup"><span data-stu-id="68ebe-131">tags to be updated</span></span>

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

### <span data-ttu-id="68ebe-132">-確認</span><span class="sxs-lookup"><span data-stu-id="68ebe-132">-Confirm</span></span>
<span data-ttu-id="68ebe-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="68ebe-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68ebe-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68ebe-134">-WhatIf</span></span>
<span data-ttu-id="68ebe-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="68ebe-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68ebe-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="68ebe-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68ebe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68ebe-137">CommonParameters</span></span>
<span data-ttu-id="68ebe-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="68ebe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68ebe-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="68ebe-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68ebe-140">輸入</span><span class="sxs-lookup"><span data-stu-id="68ebe-140">INPUTS</span></span>

### <span data-ttu-id="68ebe-141">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="68ebe-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="68ebe-142">輸出</span><span class="sxs-lookup"><span data-stu-id="68ebe-142">OUTPUTS</span></span>

### <span data-ttu-id="68ebe-143">IDesktop （DesktopVirtualization）。 Api20191210Preview。</span><span class="sxs-lookup"><span data-stu-id="68ebe-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IDesktop</span></span>

## <span data-ttu-id="68ebe-144">筆記</span><span class="sxs-lookup"><span data-stu-id="68ebe-144">NOTES</span></span>

<span data-ttu-id="68ebe-145">別名</span><span class="sxs-lookup"><span data-stu-id="68ebe-145">ALIASES</span></span>

<span data-ttu-id="68ebe-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="68ebe-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="68ebe-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="68ebe-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="68ebe-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="68ebe-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="68ebe-149">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="68ebe-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="68ebe-150">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="68ebe-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="68ebe-151">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="68ebe-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="68ebe-152">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="68ebe-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="68ebe-153">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="68ebe-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="68ebe-154">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="68ebe-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="68ebe-155">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="68ebe-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="68ebe-156">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="68ebe-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="68ebe-157">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="68ebe-157">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="68ebe-158">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="68ebe-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="68ebe-159">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="68ebe-159">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="68ebe-160">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="68ebe-160">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="68ebe-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="68ebe-161">RELATED LINKS</span></span>

