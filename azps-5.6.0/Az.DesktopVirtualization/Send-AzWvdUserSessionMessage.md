---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/send-azwvdusersessionmessage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Send-AzWvdUserSessionMessage.md
ms.openlocfilehash: 1976c5750b5372cedce8ccf237fe8a444fa1feee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905425"
---
# <span data-ttu-id="cb4c3-101">Send-AzWvdUserSessionMessage</span><span class="sxs-lookup"><span data-stu-id="cb4c3-101">Send-AzWvdUserSessionMessage</span></span>

## <span data-ttu-id="cb4c3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cb4c3-102">SYNOPSIS</span></span>
<span data-ttu-id="cb4c3-103">傳送訊息給使用者。</span><span class="sxs-lookup"><span data-stu-id="cb4c3-103">Send a message to a user.</span></span>

## <span data-ttu-id="cb4c3-104">語法</span><span class="sxs-lookup"><span data-stu-id="cb4c3-104">SYNTAX</span></span>

### <span data-ttu-id="cb4c3-105">SendExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="cb4c3-105">SendExpanded (Default)</span></span>
```
Send-AzWvdUserSessionMessage -HostPoolName <String> -ResourceGroupName <String> -SessionHostName <String>
 -UserSessionId <String> [-SubscriptionId <String>] [-MessageBody <String>] [-MessageTitle <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cb4c3-106">SendViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cb4c3-106">SendViaIdentityExpanded</span></span>
```
Send-AzWvdUserSessionMessage -InputObject <IDesktopVirtualizationIdentity> [-MessageBody <String>]
 [-MessageTitle <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cb4c3-107">描述</span><span class="sxs-lookup"><span data-stu-id="cb4c3-107">DESCRIPTION</span></span>
<span data-ttu-id="cb4c3-108">傳送訊息給使用者。</span><span class="sxs-lookup"><span data-stu-id="cb4c3-108">Send a message to a user.</span></span>

## <span data-ttu-id="cb4c3-109">例子</span><span class="sxs-lookup"><span data-stu-id="cb4c3-109">EXAMPLES</span></span>

### <span data-ttu-id="cb4c3-110">範例 1：傳送郵件至 UserSession</span><span class="sxs-lookup"><span data-stu-id="cb4c3-110">Example 1: Send a message to UserSession</span></span>
```powershell
PS C:\> Send-AzWvdUserSessionMessage -ResourceGroupName ResourceGroupName `
                                     -HostPoolName HostPoolName `
                                     -SessionHostName SessionHostName `
                                     -UserSessionId 4 `
                                     -MessageBody 'Some Message' `
                                     -MessageTitle 'Some Title'
```

<span data-ttu-id="cb4c3-111">此命令會傳送訊息至 UserSession。</span><span class="sxs-lookup"><span data-stu-id="cb4c3-111">This command sends a message to a UserSession.</span></span>

## <span data-ttu-id="cb4c3-112">參數</span><span class="sxs-lookup"><span data-stu-id="cb4c3-112">PARAMETERS</span></span>

### <span data-ttu-id="cb4c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb4c3-113">-DefaultProfile</span></span>
<span data-ttu-id="cb4c3-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cb4c3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb4c3-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="cb4c3-115">-HostPoolName</span></span>
<span data-ttu-id="cb4c3-116">指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="cb4c3-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb4c3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb4c3-117">-InputObject</span></span>
<span data-ttu-id="cb4c3-118">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="cb4c3-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: SendViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb4c3-119">-MessageBody</span><span class="sxs-lookup"><span data-stu-id="cb4c3-119">-MessageBody</span></span>
<span data-ttu-id="cb4c3-120">郵件內文。</span><span class="sxs-lookup"><span data-stu-id="cb4c3-120">Body of message.</span></span>

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

### <span data-ttu-id="cb4c3-121">-MessageTitle</span><span class="sxs-lookup"><span data-stu-id="cb4c3-121">-MessageTitle</span></span>
<span data-ttu-id="cb4c3-122">郵件標題。</span><span class="sxs-lookup"><span data-stu-id="cb4c3-122">Title of message.</span></span>

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

### <span data-ttu-id="cb4c3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb4c3-123">-PassThru</span></span>
<span data-ttu-id="cb4c3-124">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="cb4c3-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cb4c3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb4c3-125">-ResourceGroupName</span></span>
<span data-ttu-id="cb4c3-126">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb4c3-126">The name of the resource group.</span></span>
<span data-ttu-id="cb4c3-127">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="cb4c3-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb4c3-128">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="cb4c3-128">-SessionHostName</span></span>
<span data-ttu-id="cb4c3-129">指定主機集中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="cb4c3-129">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb4c3-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb4c3-130">-SubscriptionId</span></span>
<span data-ttu-id="cb4c3-131">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cb4c3-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb4c3-132">-UserSessionId</span><span class="sxs-lookup"><span data-stu-id="cb4c3-132">-UserSessionId</span></span>
<span data-ttu-id="cb4c3-133">指定工作階段主機內的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="cb4c3-133">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: SendExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb4c3-134">-確認</span><span class="sxs-lookup"><span data-stu-id="cb4c3-134">-Confirm</span></span>
<span data-ttu-id="cb4c3-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cb4c3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb4c3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb4c3-136">-WhatIf</span></span>
<span data-ttu-id="cb4c3-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb4c3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb4c3-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb4c3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb4c3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb4c3-139">CommonParameters</span></span>
<span data-ttu-id="cb4c3-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cb4c3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb4c3-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb4c3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb4c3-142">輸入</span><span class="sxs-lookup"><span data-stu-id="cb4c3-142">INPUTS</span></span>

### <span data-ttu-id="cb4c3-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="cb4c3-143">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="cb4c3-144">輸出</span><span class="sxs-lookup"><span data-stu-id="cb4c3-144">OUTPUTS</span></span>

### <span data-ttu-id="cb4c3-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cb4c3-145">System.Boolean</span></span>

## <span data-ttu-id="cb4c3-146">筆記</span><span class="sxs-lookup"><span data-stu-id="cb4c3-146">NOTES</span></span>

<span data-ttu-id="cb4c3-147">別名</span><span class="sxs-lookup"><span data-stu-id="cb4c3-147">ALIASES</span></span>

<span data-ttu-id="cb4c3-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="cb4c3-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cb4c3-149">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="cb4c3-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cb4c3-150">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="cb4c3-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cb4c3-151">INPUTOBJECT： <IDesktopVirtualizationIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="cb4c3-151">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cb4c3-152">`[ApplicationGroupName <String>]`：應用程式組的名稱</span><span class="sxs-lookup"><span data-stu-id="cb4c3-152">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="cb4c3-153">`[ApplicationName <String>]`：指定應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="cb4c3-153">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="cb4c3-154">`[DesktopName <String>]`：指定桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="cb4c3-154">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="cb4c3-155">`[HostPoolName <String>]`：指定資源群組內的主機組名</span><span class="sxs-lookup"><span data-stu-id="cb4c3-155">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="cb4c3-156">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="cb4c3-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cb4c3-157">`[MsixPackageFullName <String>]`：指定主機多工緩衝處理程式中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="cb4c3-157">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="cb4c3-158">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb4c3-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cb4c3-159">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="cb4c3-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="cb4c3-160">`[SessionHostName <String>]`：指定主機集中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="cb4c3-160">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="cb4c3-161">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cb4c3-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cb4c3-162">`[UserSessionId <String>]`：指定工作階段主機內的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="cb4c3-162">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="cb4c3-163">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="cb4c3-163">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="cb4c3-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb4c3-164">RELATED LINKS</span></span>

