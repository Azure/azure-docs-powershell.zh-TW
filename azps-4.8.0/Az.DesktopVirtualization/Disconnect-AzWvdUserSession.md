---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/disconnect-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
ms.openlocfilehash: f4156fdc52ffaf01caad49517229ebf63d960fc6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128739"
---
# <span data-ttu-id="57101-101">Disconnect-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="57101-101">Disconnect-AzWvdUserSession</span></span>

## <span data-ttu-id="57101-102">摘要</span><span class="sxs-lookup"><span data-stu-id="57101-102">SYNOPSIS</span></span>
<span data-ttu-id="57101-103">中斷 userSession 的連線。</span><span class="sxs-lookup"><span data-stu-id="57101-103">Disconnect a userSession.</span></span>

## <span data-ttu-id="57101-104">句法</span><span class="sxs-lookup"><span data-stu-id="57101-104">SYNTAX</span></span>

### <span data-ttu-id="57101-105">中斷連線 (預設) </span><span class="sxs-lookup"><span data-stu-id="57101-105">Disconnect (Default)</span></span>
```
Disconnect-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="57101-106">DisconnectViaIdentity</span><span class="sxs-lookup"><span data-stu-id="57101-106">DisconnectViaIdentity</span></span>
```
Disconnect-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="57101-107">說明</span><span class="sxs-lookup"><span data-stu-id="57101-107">DESCRIPTION</span></span>
<span data-ttu-id="57101-108">中斷 userSession 的連線。</span><span class="sxs-lookup"><span data-stu-id="57101-108">Disconnect a userSession.</span></span>

## <span data-ttu-id="57101-109">示例</span><span class="sxs-lookup"><span data-stu-id="57101-109">EXAMPLES</span></span>

### <span data-ttu-id="57101-110">範例1：依名稱中斷 Windows 虛擬桌面 UserSession 連線</span><span class="sxs-lookup"><span data-stu-id="57101-110">Example 1: Disconnect a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Disconnect-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="57101-111">這個命令會中斷工作階段主機中的 Windows 虛擬桌面 UserSession。</span><span class="sxs-lookup"><span data-stu-id="57101-111">This command disconnects a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="57101-112">參數</span><span class="sxs-lookup"><span data-stu-id="57101-112">PARAMETERS</span></span>

### <span data-ttu-id="57101-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57101-113">-DefaultProfile</span></span>
<span data-ttu-id="57101-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="57101-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57101-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="57101-115">-HostPoolName</span></span>
<span data-ttu-id="57101-116">指定資源群組中主機池的名稱</span><span class="sxs-lookup"><span data-stu-id="57101-116">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="57101-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="57101-117">-Id</span></span>
<span data-ttu-id="57101-118">指定的工作階段主機中使用者會話的名稱</span><span class="sxs-lookup"><span data-stu-id="57101-118">The name of the user session within the specified session host</span></span>

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

### <span data-ttu-id="57101-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57101-119">-InputObject</span></span>
<span data-ttu-id="57101-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="57101-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="57101-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57101-121">-PassThru</span></span>
<span data-ttu-id="57101-122">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="57101-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="57101-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57101-123">-ResourceGroupName</span></span>
<span data-ttu-id="57101-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="57101-124">The name of the resource group.</span></span>
<span data-ttu-id="57101-125">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="57101-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="57101-126">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="57101-126">-SessionHostName</span></span>
<span data-ttu-id="57101-127">指定主機池中工作階段主機的名稱</span><span class="sxs-lookup"><span data-stu-id="57101-127">The name of the session host within the specified host pool</span></span>

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

### <span data-ttu-id="57101-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57101-128">-SubscriptionId</span></span>
<span data-ttu-id="57101-129">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="57101-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="57101-130">-確認</span><span class="sxs-lookup"><span data-stu-id="57101-130">-Confirm</span></span>
<span data-ttu-id="57101-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="57101-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57101-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57101-132">-WhatIf</span></span>
<span data-ttu-id="57101-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="57101-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57101-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57101-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57101-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57101-135">CommonParameters</span></span>
<span data-ttu-id="57101-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="57101-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57101-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="57101-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57101-138">輸入</span><span class="sxs-lookup"><span data-stu-id="57101-138">INPUTS</span></span>

### <span data-ttu-id="57101-139">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="57101-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="57101-140">輸出</span><span class="sxs-lookup"><span data-stu-id="57101-140">OUTPUTS</span></span>

### <span data-ttu-id="57101-141">System.object</span><span class="sxs-lookup"><span data-stu-id="57101-141">System.Boolean</span></span>

## <span data-ttu-id="57101-142">筆記</span><span class="sxs-lookup"><span data-stu-id="57101-142">NOTES</span></span>

<span data-ttu-id="57101-143">別名</span><span class="sxs-lookup"><span data-stu-id="57101-143">ALIASES</span></span>

<span data-ttu-id="57101-144">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="57101-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="57101-145">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="57101-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57101-146">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="57101-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="57101-147">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="57101-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="57101-148">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="57101-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="57101-149">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="57101-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="57101-150">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="57101-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="57101-151">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="57101-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="57101-152">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="57101-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="57101-153">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="57101-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="57101-154">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="57101-154">The name is case insensitive.</span></span>
  - <span data-ttu-id="57101-155">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="57101-155">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="57101-156">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="57101-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="57101-157">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="57101-157">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="57101-158">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="57101-158">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="57101-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="57101-159">RELATED LINKS</span></span>
