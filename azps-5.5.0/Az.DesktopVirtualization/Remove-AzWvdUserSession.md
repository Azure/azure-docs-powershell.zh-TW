---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdUserSession.md
ms.openlocfilehash: d460b3e10ccc0e2d37a4e2aeb208d0b9f8006a10
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132035"
---
# <span data-ttu-id="2039a-101">Remove-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="2039a-101">Remove-AzWvdUserSession</span></span>

## <span data-ttu-id="2039a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2039a-102">SYNOPSIS</span></span>
<span data-ttu-id="2039a-103">移除 userSession。</span><span class="sxs-lookup"><span data-stu-id="2039a-103">Remove a userSession.</span></span>

## <span data-ttu-id="2039a-104">句法</span><span class="sxs-lookup"><span data-stu-id="2039a-104">SYNTAX</span></span>

### <span data-ttu-id="2039a-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="2039a-105">Delete (Default)</span></span>
```
Remove-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2039a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2039a-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2039a-107">說明</span><span class="sxs-lookup"><span data-stu-id="2039a-107">DESCRIPTION</span></span>
<span data-ttu-id="2039a-108">移除 userSession。</span><span class="sxs-lookup"><span data-stu-id="2039a-108">Remove a userSession.</span></span>

## <span data-ttu-id="2039a-109">示例</span><span class="sxs-lookup"><span data-stu-id="2039a-109">EXAMPLES</span></span>

### <span data-ttu-id="2039a-110">範例1：依名稱刪除 Windows 虛擬桌面 UserSession</span><span class="sxs-lookup"><span data-stu-id="2039a-110">Example 1: Delete a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Remove-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="2039a-111">這個命令會刪除工作階段主機中的 Windows 虛擬桌面 UserSession。</span><span class="sxs-lookup"><span data-stu-id="2039a-111">This command deletes a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="2039a-112">參數</span><span class="sxs-lookup"><span data-stu-id="2039a-112">PARAMETERS</span></span>

### <span data-ttu-id="2039a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2039a-113">-DefaultProfile</span></span>
<span data-ttu-id="2039a-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2039a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2039a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2039a-115">-Force</span></span>
<span data-ttu-id="2039a-116">[強制] 標記以 userSession 登入。</span><span class="sxs-lookup"><span data-stu-id="2039a-116">Force flag to login off userSession.</span></span>

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

### <span data-ttu-id="2039a-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="2039a-117">-HostPoolName</span></span>
<span data-ttu-id="2039a-118">指定資源群組中主機池的名稱</span><span class="sxs-lookup"><span data-stu-id="2039a-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="2039a-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="2039a-119">-Id</span></span>
<span data-ttu-id="2039a-120">指定的工作階段主機中使用者會話的名稱</span><span class="sxs-lookup"><span data-stu-id="2039a-120">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="2039a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2039a-121">-InputObject</span></span>
<span data-ttu-id="2039a-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2039a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2039a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2039a-123">-PassThru</span></span>
<span data-ttu-id="2039a-124">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="2039a-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2039a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2039a-125">-ResourceGroupName</span></span>
<span data-ttu-id="2039a-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2039a-126">The name of the resource group.</span></span>
<span data-ttu-id="2039a-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="2039a-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2039a-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="2039a-128">-SessionHostName</span></span>
<span data-ttu-id="2039a-129">指定主機池中工作階段主機的名稱</span><span class="sxs-lookup"><span data-stu-id="2039a-129">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="2039a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2039a-130">-SubscriptionId</span></span>
<span data-ttu-id="2039a-131">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="2039a-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2039a-132">-確認</span><span class="sxs-lookup"><span data-stu-id="2039a-132">-Confirm</span></span>
<span data-ttu-id="2039a-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2039a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2039a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2039a-134">-WhatIf</span></span>
<span data-ttu-id="2039a-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2039a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2039a-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2039a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2039a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2039a-137">CommonParameters</span></span>
<span data-ttu-id="2039a-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2039a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2039a-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2039a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2039a-140">輸入</span><span class="sxs-lookup"><span data-stu-id="2039a-140">INPUTS</span></span>

### <span data-ttu-id="2039a-141">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="2039a-141">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="2039a-142">輸出</span><span class="sxs-lookup"><span data-stu-id="2039a-142">OUTPUTS</span></span>

### <span data-ttu-id="2039a-143">System.object</span><span class="sxs-lookup"><span data-stu-id="2039a-143">System.Boolean</span></span>

## <span data-ttu-id="2039a-144">筆記</span><span class="sxs-lookup"><span data-stu-id="2039a-144">NOTES</span></span>

<span data-ttu-id="2039a-145">別名</span><span class="sxs-lookup"><span data-stu-id="2039a-145">ALIASES</span></span>

<span data-ttu-id="2039a-146">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="2039a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2039a-147">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="2039a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2039a-148">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="2039a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2039a-149">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="2039a-149">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2039a-150">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="2039a-150">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="2039a-151">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="2039a-151">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="2039a-152">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="2039a-152">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="2039a-153">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="2039a-153">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="2039a-154">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="2039a-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2039a-155">`[MsixPackageFullName <String>]`： MSIX 套件在指定 hostpool 中的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="2039a-155">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="2039a-156">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2039a-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2039a-157">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="2039a-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="2039a-158">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="2039a-158">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="2039a-159">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2039a-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2039a-160">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="2039a-160">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="2039a-161">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="2039a-161">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="2039a-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="2039a-162">RELATED LINKS</span></span>

