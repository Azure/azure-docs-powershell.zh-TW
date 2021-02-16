---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdapplicationgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdApplicationGroup.md
ms.openlocfilehash: 59ff3c3bd973e3b2189e7f06cd067eaca42870f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140967"
---
# <span data-ttu-id="564bd-101">Remove-AzWvdApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="564bd-101">Remove-AzWvdApplicationGroup</span></span>

## <span data-ttu-id="564bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="564bd-102">SYNOPSIS</span></span>
<span data-ttu-id="564bd-103">移除 applicationGroup。</span><span class="sxs-lookup"><span data-stu-id="564bd-103">Remove an applicationGroup.</span></span>

## <span data-ttu-id="564bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="564bd-104">SYNTAX</span></span>

### <span data-ttu-id="564bd-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="564bd-105">Delete (Default)</span></span>
```
Remove-AzWvdApplicationGroup -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="564bd-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="564bd-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdApplicationGroup -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="564bd-107">說明</span><span class="sxs-lookup"><span data-stu-id="564bd-107">DESCRIPTION</span></span>
<span data-ttu-id="564bd-108">移除 applicationGroup。</span><span class="sxs-lookup"><span data-stu-id="564bd-108">Remove an applicationGroup.</span></span>

## <span data-ttu-id="564bd-109">示例</span><span class="sxs-lookup"><span data-stu-id="564bd-109">EXAMPLES</span></span>

### <span data-ttu-id="564bd-110">範例1：依名稱刪除 Windows 虛擬桌面 ApplicationGroup</span><span class="sxs-lookup"><span data-stu-id="564bd-110">Example 1: Delete a Windows Virtual Desktop ApplicationGroup by name</span></span>
```powershell
PS C:\> Remove-AzWvdApplicationGroup -ResourceGroupName ResourceGroupName -Name ApplicationGroupName
```

<span data-ttu-id="564bd-111">這個命令會刪除資源群組中的 Windows 虛擬桌面 ApplicationGroup。</span><span class="sxs-lookup"><span data-stu-id="564bd-111">This command deletes a Windows Virtual Desktop ApplicationGroup in a Resource Group.</span></span>

## <span data-ttu-id="564bd-112">參數</span><span class="sxs-lookup"><span data-stu-id="564bd-112">PARAMETERS</span></span>

### <span data-ttu-id="564bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="564bd-113">-DefaultProfile</span></span>
<span data-ttu-id="564bd-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="564bd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="564bd-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="564bd-115">-InputObject</span></span>
<span data-ttu-id="564bd-116">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="564bd-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="564bd-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="564bd-117">-Name</span></span>
<span data-ttu-id="564bd-118">應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="564bd-118">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="564bd-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="564bd-119">-PassThru</span></span>
<span data-ttu-id="564bd-120">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="564bd-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="564bd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="564bd-121">-ResourceGroupName</span></span>
<span data-ttu-id="564bd-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="564bd-122">The name of the resource group.</span></span>
<span data-ttu-id="564bd-123">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="564bd-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="564bd-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="564bd-124">-SubscriptionId</span></span>
<span data-ttu-id="564bd-125">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="564bd-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="564bd-126">-確認</span><span class="sxs-lookup"><span data-stu-id="564bd-126">-Confirm</span></span>
<span data-ttu-id="564bd-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="564bd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="564bd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="564bd-128">-WhatIf</span></span>
<span data-ttu-id="564bd-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="564bd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="564bd-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="564bd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="564bd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="564bd-131">CommonParameters</span></span>
<span data-ttu-id="564bd-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="564bd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="564bd-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="564bd-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="564bd-134">輸入</span><span class="sxs-lookup"><span data-stu-id="564bd-134">INPUTS</span></span>

### <span data-ttu-id="564bd-135">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="564bd-135">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="564bd-136">輸出</span><span class="sxs-lookup"><span data-stu-id="564bd-136">OUTPUTS</span></span>

### <span data-ttu-id="564bd-137">System.object</span><span class="sxs-lookup"><span data-stu-id="564bd-137">System.Boolean</span></span>

## <span data-ttu-id="564bd-138">筆記</span><span class="sxs-lookup"><span data-stu-id="564bd-138">NOTES</span></span>

<span data-ttu-id="564bd-139">別名</span><span class="sxs-lookup"><span data-stu-id="564bd-139">ALIASES</span></span>

<span data-ttu-id="564bd-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="564bd-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="564bd-141">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="564bd-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="564bd-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="564bd-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="564bd-143">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="564bd-143">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="564bd-144">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="564bd-144">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="564bd-145">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="564bd-145">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="564bd-146">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="564bd-146">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="564bd-147">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="564bd-147">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="564bd-148">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="564bd-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="564bd-149">`[MsixPackageFullName <String>]`： MSIX 套件在指定 hostpool 中的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="564bd-149">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="564bd-150">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="564bd-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="564bd-151">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="564bd-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="564bd-152">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="564bd-152">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="564bd-153">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="564bd-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="564bd-154">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="564bd-154">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="564bd-155">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="564bd-155">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="564bd-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="564bd-156">RELATED LINKS</span></span>

