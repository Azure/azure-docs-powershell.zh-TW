---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/remove-azwvdmsixpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Remove-AzWvdMsixPackage.md
ms.openlocfilehash: 45e2c822bc21acfe69296f8d784a3a707dc1797f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98438547"
---
# <span data-ttu-id="258fb-101">Remove-AzWvdMsixPackage</span><span class="sxs-lookup"><span data-stu-id="258fb-101">Remove-AzWvdMsixPackage</span></span>

## <span data-ttu-id="258fb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="258fb-102">SYNOPSIS</span></span>
<span data-ttu-id="258fb-103">移除 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="258fb-103">Remove an MSIX Package.</span></span>

## <span data-ttu-id="258fb-104">句法</span><span class="sxs-lookup"><span data-stu-id="258fb-104">SYNTAX</span></span>

### <span data-ttu-id="258fb-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="258fb-105">Delete (Default)</span></span>
```
Remove-AzWvdMsixPackage -FullName <String> -HostPoolName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="258fb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="258fb-106">DeleteViaIdentity</span></span>
```
Remove-AzWvdMsixPackage -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="258fb-107">說明</span><span class="sxs-lookup"><span data-stu-id="258fb-107">DESCRIPTION</span></span>
<span data-ttu-id="258fb-108">移除 MSIX 套件。</span><span class="sxs-lookup"><span data-stu-id="258fb-108">Remove an MSIX Package.</span></span>

## <span data-ttu-id="258fb-109">示例</span><span class="sxs-lookup"><span data-stu-id="258fb-109">EXAMPLES</span></span>

### <span data-ttu-id="258fb-110">範例1：依套件完整名稱刪除 MSIX 套件</span><span class="sxs-lookup"><span data-stu-id="258fb-110">Example 1: Delete MSIX Package by Package Full Name</span></span>
```powershell
PS C:\> Remove-AzWvdMsixPackage -HostPoolName HostPoolName -ResourceGroupName ResourceGroupName -SubscriptionId SubscriptionId -FullName PackageFullName
```

<span data-ttu-id="258fb-111">這個命令會刪除 HostPool 中的 MSIX 套件</span><span class="sxs-lookup"><span data-stu-id="258fb-111">This command deletes a MSIX Package in a HostPool</span></span>

## <span data-ttu-id="258fb-112">參數</span><span class="sxs-lookup"><span data-stu-id="258fb-112">PARAMETERS</span></span>

### <span data-ttu-id="258fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="258fb-113">-DefaultProfile</span></span>
<span data-ttu-id="258fb-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="258fb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="258fb-115">-FullName</span><span class="sxs-lookup"><span data-stu-id="258fb-115">-FullName</span></span>
<span data-ttu-id="258fb-116">指定 hostpool 中 MSIX 套件的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="258fb-116">The version specific package full name of the MSIX package within specified hostpool</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: MsixPackageFullName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="258fb-117">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="258fb-117">-HostPoolName</span></span>
<span data-ttu-id="258fb-118">指定資源群組中主機池的名稱</span><span class="sxs-lookup"><span data-stu-id="258fb-118">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="258fb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="258fb-119">-InputObject</span></span>
<span data-ttu-id="258fb-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="258fb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="258fb-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="258fb-121">-PassThru</span></span>
<span data-ttu-id="258fb-122">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="258fb-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="258fb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="258fb-123">-ResourceGroupName</span></span>
<span data-ttu-id="258fb-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="258fb-124">The name of the resource group.</span></span>
<span data-ttu-id="258fb-125">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="258fb-125">The name is case insensitive.</span></span>

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

### <span data-ttu-id="258fb-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="258fb-126">-SubscriptionId</span></span>
<span data-ttu-id="258fb-127">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="258fb-127">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="258fb-128">-確認</span><span class="sxs-lookup"><span data-stu-id="258fb-128">-Confirm</span></span>
<span data-ttu-id="258fb-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="258fb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="258fb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="258fb-130">-WhatIf</span></span>
<span data-ttu-id="258fb-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="258fb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="258fb-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="258fb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="258fb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="258fb-133">CommonParameters</span></span>
<span data-ttu-id="258fb-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="258fb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="258fb-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="258fb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="258fb-136">輸入</span><span class="sxs-lookup"><span data-stu-id="258fb-136">INPUTS</span></span>

### <span data-ttu-id="258fb-137">IDesktopVirtualizationIdentity （DesktopVirtualization）的</span><span class="sxs-lookup"><span data-stu-id="258fb-137">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="258fb-138">輸出</span><span class="sxs-lookup"><span data-stu-id="258fb-138">OUTPUTS</span></span>

### <span data-ttu-id="258fb-139">System.object</span><span class="sxs-lookup"><span data-stu-id="258fb-139">System.Boolean</span></span>

## <span data-ttu-id="258fb-140">筆記</span><span class="sxs-lookup"><span data-stu-id="258fb-140">NOTES</span></span>

<span data-ttu-id="258fb-141">別名</span><span class="sxs-lookup"><span data-stu-id="258fb-141">ALIASES</span></span>

<span data-ttu-id="258fb-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="258fb-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="258fb-143">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="258fb-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="258fb-144">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="258fb-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="258fb-145">INPUTOBJECT <IDesktopVirtualizationIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="258fb-145">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="258fb-146">`[ApplicationGroupName <String>]`：應用程式群組的名稱</span><span class="sxs-lookup"><span data-stu-id="258fb-146">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="258fb-147">`[ApplicationName <String>]`：指定的應用程式群組中的應用程式名稱</span><span class="sxs-lookup"><span data-stu-id="258fb-147">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="258fb-148">`[DesktopName <String>]`：指定的桌面群組中的桌面名稱</span><span class="sxs-lookup"><span data-stu-id="258fb-148">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="258fb-149">`[HostPoolName <String>]`：指定資源群組中的主機池名稱</span><span class="sxs-lookup"><span data-stu-id="258fb-149">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="258fb-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="258fb-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="258fb-151">`[MsixPackageFullName <String>]`： MSIX 套件在指定 hostpool 中的版本特定套件完整名稱</span><span class="sxs-lookup"><span data-stu-id="258fb-151">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="258fb-152">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="258fb-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="258fb-153">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="258fb-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="258fb-154">`[SessionHostName <String>]`：位於指定主機池中的工作階段主機名稱</span><span class="sxs-lookup"><span data-stu-id="258fb-154">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="258fb-155">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="258fb-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="258fb-156">`[UserSessionId <String>]`：指定工作階段主機中的使用者會話名稱</span><span class="sxs-lookup"><span data-stu-id="258fb-156">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="258fb-157">`[WorkspaceName <String>]`：工作區的名稱</span><span class="sxs-lookup"><span data-stu-id="258fb-157">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="258fb-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="258fb-158">RELATED LINKS</span></span>

