---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdHostPool.md
ms.openlocfilehash: 65e7d5870e03d4e2d103254aec7a44835286d5df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139263"
---
# <span data-ttu-id="324cd-101">Remove-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="324cd-101">Remove-AzWvdHostPool</span></span>

## <span data-ttu-id="324cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="324cd-102">SYNOPSIS</span></span>
<span data-ttu-id="324cd-103">移除主機池。</span><span class="sxs-lookup"><span data-stu-id="324cd-103">Remove a host pool.</span></span>

## <span data-ttu-id="324cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="324cd-104">SYNTAX</span></span>

### <span data-ttu-id="324cd-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="324cd-105">Delete (Default)</span></span>
```
Remove-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="324cd-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="324cd-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="324cd-107">說明</span><span class="sxs-lookup"><span data-stu-id="324cd-107">DESCRIPTION</span></span>
<span data-ttu-id="324cd-108">移除主機池。</span><span class="sxs-lookup"><span data-stu-id="324cd-108">Remove a host pool.</span></span>

## <span data-ttu-id="324cd-109">示例</span><span class="sxs-lookup"><span data-stu-id="324cd-109">EXAMPLES</span></span>

### <span data-ttu-id="324cd-110">範例1：依名稱刪除 Windows 虛擬桌面 HostPool</span><span class="sxs-lookup"><span data-stu-id="324cd-110">Example 1: Delete a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Remove-AzWvdHostPool -ResourceGroupName ResourceGroupName -Name HostPoolName
```

<span data-ttu-id="324cd-111">這個命令會刪除資源群組中的 Windows 虛擬桌面 HostPool。</span><span class="sxs-lookup"><span data-stu-id="324cd-111">This command deletes a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="324cd-112">參數</span><span class="sxs-lookup"><span data-stu-id="324cd-112">PARAMETERS</span></span>

### <span data-ttu-id="324cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="324cd-113">-DefaultProfile</span></span>
<span data-ttu-id="324cd-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="324cd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="324cd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="324cd-115">-Force</span></span>
<span data-ttu-id="324cd-116">[強制] 標記以刪除 sessionHost。</span><span class="sxs-lookup"><span data-stu-id="324cd-116">Force flag to delete sessionHost.</span></span>

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

### <span data-ttu-id="324cd-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="324cd-117">-InputObject</span></span>
<span data-ttu-id="324cd-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="324cd-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="324cd-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="324cd-119">-Name</span></span>
<span data-ttu-id="324cd-120">指定資源群組中主機池的名稱</span><span class="sxs-lookup"><span data-stu-id="324cd-120">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="324cd-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="324cd-121">-PassThru</span></span>
<span data-ttu-id="324cd-122">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="324cd-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="324cd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="324cd-123">-ResourceGroupName</span></span>
<span data-ttu-id="324cd-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="324cd-124">The name of the resource group.</span></span>
<span data-ttu-id="324cd-125">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="324cd-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="324cd-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="324cd-126">-SubscriptionId</span></span>
<span data-ttu-id="324cd-127">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="324cd-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="324cd-128">-確認</span><span class="sxs-lookup"><span data-stu-id="324cd-128">-Confirm</span></span>
<span data-ttu-id="324cd-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="324cd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="324cd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="324cd-130">-WhatIf</span></span>
<span data-ttu-id="324cd-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="324cd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="324cd-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="324cd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="324cd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="324cd-133">CommonParameters</span></span>
<span data-ttu-id="324cd-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="324cd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="324cd-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="324cd-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="324cd-136">輸入</span><span class="sxs-lookup"><span data-stu-id="324cd-136">INPUTS</span></span>

### <span data-ttu-id="324cd-137">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="324cd-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="324cd-138">輸出</span><span class="sxs-lookup"><span data-stu-id="324cd-138">OUTPUTS</span></span>

### <span data-ttu-id="324cd-139">System.object</span><span class="sxs-lookup"><span data-stu-id="324cd-139">System.Boolean</span></span>

## <span data-ttu-id="324cd-140">筆記</span><span class="sxs-lookup"><span data-stu-id="324cd-140">NOTES</span></span>

<span data-ttu-id="324cd-141">別名</span><span class="sxs-lookup"><span data-stu-id="324cd-141">ALIASES</span></span>

<span data-ttu-id="324cd-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="324cd-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="324cd-143">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="324cd-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="324cd-144">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="324cd-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="324cd-145">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="324cd-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="324cd-146">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="324cd-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="324cd-147">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="324cd-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="324cd-148">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="324cd-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="324cd-149">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="324cd-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="324cd-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="324cd-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="324cd-151">`[MsixPackageFullName <String>]`： MSIX 套件在指定 hostpool 中的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="324cd-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="324cd-152">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="324cd-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="324cd-153">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="324cd-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="324cd-154">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="324cd-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="324cd-155">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="324cd-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="324cd-156">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="324cd-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="324cd-157">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="324cd-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="324cd-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="324cd-158">RELATED LINKS</span></span>

