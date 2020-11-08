---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplicationGroup.md
ms.openlocfilehash: ab1f338be9d983efceac0045fec96b1a63fb66bf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138931"
---
# <span data-ttu-id="36912-101">Update-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="36912-101">Update-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="36912-102">摘要</span><span class="sxs-lookup"><span data-stu-id="36912-102">SYNOPSIS</span></span>
<span data-ttu-id="36912-103">更新 applicationGroup。</span><span class="sxs-lookup"><span data-stu-id="36912-103">Update an applicationGroup.</span></span>

## <span data-ttu-id="36912-104">句法</span><span class="sxs-lookup"><span data-stu-id="36912-104">SYNTAX</span></span>

### <span data-ttu-id="36912-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="36912-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="36912-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="36912-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-Description <String>]
 [-FriendlyName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="36912-107">說明</span><span class="sxs-lookup"><span data-stu-id="36912-107">DESCRIPTION</span></span>
<span data-ttu-id="36912-108">更新 applicationGroup。</span><span class="sxs-lookup"><span data-stu-id="36912-108">Update an applicationGroup.</span></span>

## <span data-ttu-id="36912-109">示例</span><span class="sxs-lookup"><span data-stu-id="36912-109">EXAMPLES</span></span>

### <span data-ttu-id="36912-110">範例1：依名稱建立 Windows 虛擬桌面 ApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="36912-110">Example 1: Create a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> New-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName `
                            -Name ApplicationGroupName `
                            -FriendlyName 'Friendly Name' `
                            -Description 'Description' `

Location   Name                 Type
--------   ----                 ----
eastus     ApplicationGroupName Microsoft.DesktopVirtualization/applicationgroups
```

<span data-ttu-id="36912-111">這個命令會在資源群組中建立 Windows 虛擬桌面 ApplicationGroup。</span><span class="sxs-lookup"><span data-stu-id="36912-111">This command creates a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="36912-112">參數</span><span class="sxs-lookup"><span data-stu-id="36912-112">PARAMETERS</span></span>

### <span data-ttu-id="36912-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36912-113">-DefaultProfile</span></span>
<span data-ttu-id="36912-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="36912-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36912-115">-描述</span><span class="sxs-lookup"><span data-stu-id="36912-115">-Description</span></span>
<span data-ttu-id="36912-116">ApplicationGroup 的描述。</span><span class="sxs-lookup"><span data-stu-id="36912-116">Description of ApplicationGroup.</span></span>

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

### <span data-ttu-id="36912-117">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="36912-117">-FriendlyName</span></span>
<span data-ttu-id="36912-118">ApplicationGroup 的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="36912-118">Friendly name of ApplicationGroup.</span></span>

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

### <span data-ttu-id="36912-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36912-119">-InputObject</span></span>
<span data-ttu-id="36912-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="36912-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="36912-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="36912-121">-Name</span></span>
<span data-ttu-id="36912-122">應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="36912-122">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36912-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36912-123">-ResourceGroupName</span></span>
<span data-ttu-id="36912-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="36912-124">The name of the resource group.</span></span>
<span data-ttu-id="36912-125">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="36912-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="36912-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36912-126">-SubscriptionId</span></span>
<span data-ttu-id="36912-127">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="36912-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="36912-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="36912-128">-Tag</span></span>
<span data-ttu-id="36912-129">要更新的標記</span><span class="sxs-lookup"><span data-stu-id="36912-129">tags to be updated</span></span>

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

### <span data-ttu-id="36912-130">-確認</span><span class="sxs-lookup"><span data-stu-id="36912-130">-Confirm</span></span>
<span data-ttu-id="36912-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="36912-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36912-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36912-132">-WhatIf</span></span>
<span data-ttu-id="36912-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="36912-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36912-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36912-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36912-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36912-135">CommonParameters</span></span>
<span data-ttu-id="36912-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="36912-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36912-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="36912-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36912-138">輸入</span><span class="sxs-lookup"><span data-stu-id="36912-138">INPUTS</span></span>

### <span data-ttu-id="36912-139">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="36912-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="36912-140">輸出</span><span class="sxs-lookup"><span data-stu-id="36912-140">OUTPUTS</span></span>

### <span data-ttu-id="36912-141">IApplicationGroup （DesktopVirtualization）。 Api20191210Preview。</span><span class="sxs-lookup"><span data-stu-id="36912-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplicationGroup</span></span>

## <span data-ttu-id="36912-142">筆記</span><span class="sxs-lookup"><span data-stu-id="36912-142">NOTES</span></span>

<span data-ttu-id="36912-143">別名</span><span class="sxs-lookup"><span data-stu-id="36912-143">ALIASES</span></span>

<span data-ttu-id="36912-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="36912-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="36912-145">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="36912-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="36912-146">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="36912-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="36912-147">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="36912-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="36912-148">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="36912-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="36912-149">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="36912-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="36912-150">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="36912-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="36912-151">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="36912-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="36912-152">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="36912-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="36912-153">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="36912-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="36912-154">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="36912-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="36912-155">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="36912-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="36912-156">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="36912-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="36912-157">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="36912-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="36912-158">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="36912-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="36912-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="36912-159">RELATED LINKS</span></span>

