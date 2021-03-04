---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/remove-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
ms.openlocfilehash: 42902280d93797613197f7da3263418e0fc8672e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905430"
---
# <span data-ttu-id="4b531-101">Remove-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="4b531-101">Remove-AzWvdHostPool</span></span>

## <span data-ttu-id="4b531-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4b531-102">SYNOPSIS</span></span>
<span data-ttu-id="4b531-103">移除主機區。</span><span class="sxs-lookup"><span data-stu-id="4b531-103">Remove a host pool.</span></span>

## <span data-ttu-id="4b531-104">語法</span><span class="sxs-lookup"><span data-stu-id="4b531-104">SYNTAX</span></span>

### <span data-ttu-id="4b531-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="4b531-105">Delete (Default)</span></span>
```
Remove-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4b531-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4b531-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4b531-107">描述</span><span class="sxs-lookup"><span data-stu-id="4b531-107">DESCRIPTION</span></span>
<span data-ttu-id="4b531-108">移除主機區。</span><span class="sxs-lookup"><span data-stu-id="4b531-108">Remove a host pool.</span></span>

## <span data-ttu-id="4b531-109">例子</span><span class="sxs-lookup"><span data-stu-id="4b531-109">EXAMPLES</span></span>

### <span data-ttu-id="4b531-110">範例 1：刪除 Windows 虛擬桌面主機多工緩衝處理程式的名稱</span><span class="sxs-lookup"><span data-stu-id="4b531-110">Example 1: Delete a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Remove-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName
```

<span data-ttu-id="4b531-111">此命令會刪除資源群組中的 Windows 虛擬桌面主機後臺。</span><span class="sxs-lookup"><span data-stu-id="4b531-111">This command deletes a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="4b531-112">參數</span><span class="sxs-lookup"><span data-stu-id="4b531-112">PARAMETERS</span></span>

### <span data-ttu-id="4b531-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b531-113">-DefaultProfile</span></span>
<span data-ttu-id="4b531-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4b531-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b531-115">-強制</span><span class="sxs-lookup"><span data-stu-id="4b531-115">-Force</span></span>
<span data-ttu-id="4b531-116">強制標標以刪除工作階段主機。</span><span class="sxs-lookup"><span data-stu-id="4b531-116">Force flag to delete sessionHost.</span></span>

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

### <span data-ttu-id="4b531-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b531-117">-InputObject</span></span>
<span data-ttu-id="4b531-118">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4b531-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4b531-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="4b531-119">-Name</span></span>
<span data-ttu-id="4b531-120">指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="4b531-120">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b531-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b531-121">-PassThru</span></span>
<span data-ttu-id="4b531-122">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="4b531-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4b531-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b531-123">-ResourceGroupName</span></span>
<span data-ttu-id="4b531-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b531-124">The name of the resource group.</span></span>
<span data-ttu-id="4b531-125">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="4b531-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4b531-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4b531-126">-SubscriptionId</span></span>
<span data-ttu-id="4b531-127">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4b531-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4b531-128">-確認</span><span class="sxs-lookup"><span data-stu-id="4b531-128">-Confirm</span></span>
<span data-ttu-id="4b531-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4b531-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b531-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b531-130">-WhatIf</span></span>
<span data-ttu-id="4b531-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4b531-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b531-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4b531-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b531-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b531-133">CommonParameters</span></span>
<span data-ttu-id="4b531-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4b531-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b531-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b531-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b531-136">輸入</span><span class="sxs-lookup"><span data-stu-id="4b531-136">INPUTS</span></span>

### <span data-ttu-id="4b531-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="4b531-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="4b531-138">輸出</span><span class="sxs-lookup"><span data-stu-id="4b531-138">OUTPUTS</span></span>

### <span data-ttu-id="4b531-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4b531-139">System.Boolean</span></span>

## <span data-ttu-id="4b531-140">筆記</span><span class="sxs-lookup"><span data-stu-id="4b531-140">NOTES</span></span>

<span data-ttu-id="4b531-141">別名</span><span class="sxs-lookup"><span data-stu-id="4b531-141">ALIASES</span></span>

<span data-ttu-id="4b531-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="4b531-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4b531-143">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4b531-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4b531-144">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="4b531-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4b531-145">INPUTOBJECT： <IDesktopVirtualizationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="4b531-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4b531-146">`[ApplicationGroupName <String>]`：應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="4b531-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="4b531-147">`[ApplicationName <String>]`：指定應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="4b531-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="4b531-148">`[DesktopName <String>]`：指定桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="4b531-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="4b531-149">`[HostPoolName <String>]`：指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="4b531-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="4b531-150">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="4b531-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4b531-151">`[MsixPackageFullName <String>]`：指定主機多工緩衝處理程式中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="4b531-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="4b531-152">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b531-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4b531-153">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="4b531-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="4b531-154">`[SessionHostName <String>]`：指定主機集中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="4b531-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="4b531-155">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4b531-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4b531-156">`[UserSessionId <String>]`：指定工作階段主機內的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="4b531-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="4b531-157">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="4b531-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="4b531-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b531-158">RELATED LINKS</span></span>

