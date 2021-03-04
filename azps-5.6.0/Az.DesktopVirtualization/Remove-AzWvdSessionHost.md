---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdsessionhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdSessionHost.md
ms.openlocfilehash: ee8334a233c35c2b834bfb89ddf20152d466367f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905422"
---
# <span data-ttu-id="c3b30-101">Remove-AzWvdSessionHost</span><span class="sxs-lookup"><span data-stu-id="c3b30-101">Remove-AzWvdSessionHost</span></span>

## <span data-ttu-id="c3b30-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c3b30-102">SYNOPSIS</span></span>
<span data-ttu-id="c3b30-103">移除 SessionHost。</span><span class="sxs-lookup"><span data-stu-id="c3b30-103">Remove a SessionHost.</span></span>

## <span data-ttu-id="c3b30-104">語法</span><span class="sxs-lookup"><span data-stu-id="c3b30-104">SYNTAX</span></span>

### <span data-ttu-id="c3b30-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="c3b30-105">Delete (Default)</span></span>
```
Remove-AzWvdSessionHost -HostPoolName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c3b30-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c3b30-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdSessionHost -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c3b30-107">描述</span><span class="sxs-lookup"><span data-stu-id="c3b30-107">DESCRIPTION</span></span>
<span data-ttu-id="c3b30-108">移除 SessionHost。</span><span class="sxs-lookup"><span data-stu-id="c3b30-108">Remove a SessionHost.</span></span>

## <span data-ttu-id="c3b30-109">例子</span><span class="sxs-lookup"><span data-stu-id="c3b30-109">EXAMPLES</span></span>

### <span data-ttu-id="c3b30-110">範例 1：刪除 Windows 虛擬桌面工作階段主機名</span><span class="sxs-lookup"><span data-stu-id="c3b30-110">Example 1: Delete a Windows Virtual Desktop SessionHost by name</span></span>
```powershell
PS C:\> Remove-AzWvdSessionHost -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -Name SessionHostName
```

<span data-ttu-id="c3b30-111">此命令會刪除主機集中的 Windows 虛擬桌面工作階段主機。</span><span class="sxs-lookup"><span data-stu-id="c3b30-111">This command deletes a Windows Virtual Desktop SessionHost in a Host Pool.</span></span>

## <span data-ttu-id="c3b30-112">參數</span><span class="sxs-lookup"><span data-stu-id="c3b30-112">PARAMETERS</span></span>

### <span data-ttu-id="c3b30-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3b30-113">-DefaultProfile</span></span>
<span data-ttu-id="c3b30-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c3b30-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3b30-115">-強制</span><span class="sxs-lookup"><span data-stu-id="c3b30-115">-Force</span></span>
<span data-ttu-id="c3b30-116">強制標標以強制刪除工作階段主機，即使使用者Session存在也一樣。</span><span class="sxs-lookup"><span data-stu-id="c3b30-116">Force flag to force sessionHost deletion even when userSession exists.</span></span>

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

### <span data-ttu-id="c3b30-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="c3b30-117">-HostPoolName</span></span>
<span data-ttu-id="c3b30-118">指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="c3b30-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="c3b30-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3b30-119">-InputObject</span></span>
<span data-ttu-id="c3b30-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c3b30-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c3b30-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="c3b30-121">-Name</span></span>
<span data-ttu-id="c3b30-122">指定主機集中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="c3b30-122">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: SessionHostName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b30-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3b30-123">-PassThru</span></span>
<span data-ttu-id="c3b30-124">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="c3b30-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c3b30-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3b30-125">-ResourceGroupName</span></span>
<span data-ttu-id="c3b30-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3b30-126">The name of the resource group.</span></span>
<span data-ttu-id="c3b30-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c3b30-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c3b30-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c3b30-128">-SubscriptionId</span></span>
<span data-ttu-id="c3b30-129">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3b30-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c3b30-130">-確認</span><span class="sxs-lookup"><span data-stu-id="c3b30-130">-Confirm</span></span>
<span data-ttu-id="c3b30-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c3b30-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3b30-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3b30-132">-WhatIf</span></span>
<span data-ttu-id="c3b30-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c3b30-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3b30-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c3b30-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3b30-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3b30-135">CommonParameters</span></span>
<span data-ttu-id="c3b30-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c3b30-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3b30-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c3b30-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3b30-138">輸入</span><span class="sxs-lookup"><span data-stu-id="c3b30-138">INPUTS</span></span>

### <span data-ttu-id="c3b30-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="c3b30-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="c3b30-140">輸出</span><span class="sxs-lookup"><span data-stu-id="c3b30-140">OUTPUTS</span></span>

### <span data-ttu-id="c3b30-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c3b30-141">System.Boolean</span></span>

## <span data-ttu-id="c3b30-142">筆記</span><span class="sxs-lookup"><span data-stu-id="c3b30-142">NOTES</span></span>

<span data-ttu-id="c3b30-143">別名</span><span class="sxs-lookup"><span data-stu-id="c3b30-143">ALIASES</span></span>

<span data-ttu-id="c3b30-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="c3b30-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c3b30-145">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c3b30-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c3b30-146">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="c3b30-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c3b30-147">INPUTOBJECT： <IDesktopVirtualizationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="c3b30-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c3b30-148">`[ApplicationGroupName <String>]`：應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="c3b30-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="c3b30-149">`[ApplicationName <String>]`：指定應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="c3b30-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="c3b30-150">`[DesktopName <String>]`：指定桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="c3b30-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="c3b30-151">`[HostPoolName <String>]`：指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="c3b30-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="c3b30-152">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="c3b30-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c3b30-153">`[MsixPackageFullName <String>]`：指定主機多工緩衝處理程式中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="c3b30-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="c3b30-154">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3b30-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c3b30-155">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c3b30-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="c3b30-156">`[SessionHostName <String>]`：指定主機集中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="c3b30-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="c3b30-157">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3b30-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c3b30-158">`[UserSessionId <String>]`：指定工作階段主機內的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="c3b30-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="c3b30-159">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="c3b30-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="c3b30-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3b30-160">RELATED LINKS</span></span>

