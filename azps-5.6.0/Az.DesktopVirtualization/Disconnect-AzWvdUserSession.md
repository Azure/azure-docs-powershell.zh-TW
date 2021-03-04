---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/disconnect-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
ms.openlocfilehash: 61e1eb1f5ae3846ce2f0cf7ad82d17d613d27e0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905473"
---
# <span data-ttu-id="b10d7-101">Disconnect-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="b10d7-101">Disconnect-AzWvdUserSession</span></span>

## <span data-ttu-id="b10d7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b10d7-102">SYNOPSIS</span></span>
<span data-ttu-id="b10d7-103">中斷使用者中斷連接。</span><span class="sxs-lookup"><span data-stu-id="b10d7-103">Disconnect a userSession.</span></span>

## <span data-ttu-id="b10d7-104">語法</span><span class="sxs-lookup"><span data-stu-id="b10d7-104">SYNTAX</span></span>

### <span data-ttu-id="b10d7-105">中斷 (預設) </span><span class="sxs-lookup"><span data-stu-id="b10d7-105">Disconnect (Default)</span></span>
```
Disconnect-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b10d7-106">DisconnectViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b10d7-106">DisconnectViaIdentity</span></span>
```
Disconnect-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b10d7-107">描述</span><span class="sxs-lookup"><span data-stu-id="b10d7-107">DESCRIPTION</span></span>
<span data-ttu-id="b10d7-108">中斷使用者中斷連接。</span><span class="sxs-lookup"><span data-stu-id="b10d7-108">Disconnect a userSession.</span></span>

## <span data-ttu-id="b10d7-109">例子</span><span class="sxs-lookup"><span data-stu-id="b10d7-109">EXAMPLES</span></span>

### <span data-ttu-id="b10d7-110">範例 1：中斷 Windows 虛擬桌面使用者名稱的中斷連接</span><span class="sxs-lookup"><span data-stu-id="b10d7-110">Example 1: Disconnect a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Disconnect-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="b10d7-111">此命令會中斷工作階段主機中的 Windows 虛擬桌面使用者服務。</span><span class="sxs-lookup"><span data-stu-id="b10d7-111">This command disconnects a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="b10d7-112">參數</span><span class="sxs-lookup"><span data-stu-id="b10d7-112">PARAMETERS</span></span>

### <span data-ttu-id="b10d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b10d7-113">-DefaultProfile</span></span>
<span data-ttu-id="b10d7-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b10d7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b10d7-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="b10d7-115">-HostPoolName</span></span>
<span data-ttu-id="b10d7-116">指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="b10d7-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b10d7-117">-Id</span><span class="sxs-lookup"><span data-stu-id="b10d7-117">-Id</span></span>
<span data-ttu-id="b10d7-118">指定工作階段主機內的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="b10d7-118">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b10d7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b10d7-119">-InputObject</span></span>
<span data-ttu-id="b10d7-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b10d7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DisconnectViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b10d7-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b10d7-121">-PassThru</span></span>
<span data-ttu-id="b10d7-122">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="b10d7-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b10d7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b10d7-123">-ResourceGroupName</span></span>
<span data-ttu-id="b10d7-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b10d7-124">The name of the resource group.</span></span>
<span data-ttu-id="b10d7-125">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b10d7-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b10d7-126">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="b10d7-126">-SessionHostName</span></span>
<span data-ttu-id="b10d7-127">指定主機集中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="b10d7-127">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b10d7-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b10d7-128">-SubscriptionId</span></span>
<span data-ttu-id="b10d7-129">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b10d7-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b10d7-130">-確認</span><span class="sxs-lookup"><span data-stu-id="b10d7-130">-Confirm</span></span>
<span data-ttu-id="b10d7-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b10d7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b10d7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b10d7-132">-WhatIf</span></span>
<span data-ttu-id="b10d7-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b10d7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b10d7-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b10d7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b10d7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b10d7-135">CommonParameters</span></span>
<span data-ttu-id="b10d7-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b10d7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b10d7-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b10d7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b10d7-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b10d7-138">INPUTS</span></span>

### <span data-ttu-id="b10d7-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="b10d7-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="b10d7-140">輸出</span><span class="sxs-lookup"><span data-stu-id="b10d7-140">OUTPUTS</span></span>

### <span data-ttu-id="b10d7-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b10d7-141">System.Boolean</span></span>

## <span data-ttu-id="b10d7-142">筆記</span><span class="sxs-lookup"><span data-stu-id="b10d7-142">NOTES</span></span>

<span data-ttu-id="b10d7-143">別名</span><span class="sxs-lookup"><span data-stu-id="b10d7-143">ALIASES</span></span>

<span data-ttu-id="b10d7-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b10d7-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b10d7-145">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b10d7-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b10d7-146">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b10d7-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b10d7-147">INPUTOBJECT： <IDesktopVirtualizationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b10d7-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b10d7-148">`[ApplicationGroupName <String>]`：應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="b10d7-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="b10d7-149">`[ApplicationName <String>]`：指定應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="b10d7-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="b10d7-150">`[DesktopName <String>]`：指定桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="b10d7-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="b10d7-151">`[HostPoolName <String>]`：指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="b10d7-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="b10d7-152">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="b10d7-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b10d7-153">`[MsixPackageFullName <String>]`：指定主機多工緩衝處理程式中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="b10d7-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="b10d7-154">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b10d7-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b10d7-155">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="b10d7-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="b10d7-156">`[SessionHostName <String>]`：指定主機集中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="b10d7-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="b10d7-157">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b10d7-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b10d7-158">`[UserSessionId <String>]`：指定工作階段主機內的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="b10d7-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="b10d7-159">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="b10d7-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="b10d7-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="b10d7-160">RELATED LINKS</span></span>

