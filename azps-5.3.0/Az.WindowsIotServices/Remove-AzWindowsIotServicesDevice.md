---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/remove-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 265c0e68dd3f19afbefd8cf993e058f56e3ec9f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435932"
---
# <span data-ttu-id="c30ab-101">Remove-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="c30ab-101">Remove-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="c30ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c30ab-102">SYNOPSIS</span></span>
<span data-ttu-id="c30ab-103">刪除 Windows IoT 裝置服務。</span><span class="sxs-lookup"><span data-stu-id="c30ab-103">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="c30ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="c30ab-104">SYNTAX</span></span>

### <span data-ttu-id="c30ab-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="c30ab-105">Delete (Default)</span></span>
```
Remove-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c30ab-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c30ab-106">DeleteViaIdentity</span></span>
```
Remove-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c30ab-107">說明</span><span class="sxs-lookup"><span data-stu-id="c30ab-107">DESCRIPTION</span></span>
<span data-ttu-id="c30ab-108">刪除 Windows IoT 裝置服務。</span><span class="sxs-lookup"><span data-stu-id="c30ab-108">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="c30ab-109">示例</span><span class="sxs-lookup"><span data-stu-id="c30ab-109">EXAMPLES</span></span>

### <span data-ttu-id="c30ab-110">範例1：依名稱移除 Windows IoT 服務</span><span class="sxs-lookup"><span data-stu-id="c30ab-110">Example 1: Remove a Windows IoT services by name</span></span>
```powershell
PS C:\> Remove-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test

```

<span data-ttu-id="c30ab-111">這個命令會依名稱移除 Windows IoT 服務。</span><span class="sxs-lookup"><span data-stu-id="c30ab-111">This command removes a Windows IoT services by name.</span></span>

### <span data-ttu-id="c30ab-112">範例2：依管道移除 Windows IoT 服務</span><span class="sxs-lookup"><span data-stu-id="c30ab-112">Example 2: Remove a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01 | Remove-AzWindowsIotServicesDevice


```

<span data-ttu-id="c30ab-113">這個命令會依管道移除 Windows IoT 服務。</span><span class="sxs-lookup"><span data-stu-id="c30ab-113">This command removes a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="c30ab-114">參數</span><span class="sxs-lookup"><span data-stu-id="c30ab-114">PARAMETERS</span></span>

### <span data-ttu-id="c30ab-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c30ab-115">-DefaultProfile</span></span>
<span data-ttu-id="c30ab-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c30ab-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c30ab-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c30ab-117">-InputObject</span></span>
<span data-ttu-id="c30ab-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c30ab-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c30ab-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c30ab-119">-Name</span></span>
<span data-ttu-id="c30ab-120">Windows IoT 裝置服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="c30ab-120">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="c30ab-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c30ab-121">-ResourceGroupName</span></span>
<span data-ttu-id="c30ab-122">包含 Windows IoT 裝置服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c30ab-122">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="c30ab-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c30ab-123">-SubscriptionId</span></span>
<span data-ttu-id="c30ab-124">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="c30ab-124">The subscription identifier.</span></span>

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

### <span data-ttu-id="c30ab-125">-確認</span><span class="sxs-lookup"><span data-stu-id="c30ab-125">-Confirm</span></span>
<span data-ttu-id="c30ab-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c30ab-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c30ab-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c30ab-127">-WhatIf</span></span>
<span data-ttu-id="c30ab-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c30ab-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c30ab-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c30ab-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c30ab-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c30ab-130">CommonParameters</span></span>
<span data-ttu-id="c30ab-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c30ab-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c30ab-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c30ab-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c30ab-133">輸入</span><span class="sxs-lookup"><span data-stu-id="c30ab-133">INPUTS</span></span>

### <span data-ttu-id="c30ab-134">IWindowsIotServicesIdentity （WindowsIotServices）的</span><span class="sxs-lookup"><span data-stu-id="c30ab-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="c30ab-135">輸出</span><span class="sxs-lookup"><span data-stu-id="c30ab-135">OUTPUTS</span></span>

### <span data-ttu-id="c30ab-136">IDeviceService （WindowsIotServices）。 Api20190601。</span><span class="sxs-lookup"><span data-stu-id="c30ab-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="c30ab-137">筆記</span><span class="sxs-lookup"><span data-stu-id="c30ab-137">NOTES</span></span>

<span data-ttu-id="c30ab-138">別名</span><span class="sxs-lookup"><span data-stu-id="c30ab-138">ALIASES</span></span>

<span data-ttu-id="c30ab-139">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="c30ab-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c30ab-140">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="c30ab-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c30ab-141">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="c30ab-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c30ab-142">INPUTOBJECT <IWindowsIotServicesIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="c30ab-142">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c30ab-143">`[DeviceName <String>]`： Windows IoT 裝置服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="c30ab-143">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="c30ab-144">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="c30ab-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c30ab-145">`[ResourceGroupName <String>]`：包含 Windows IoT 裝置服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c30ab-145">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="c30ab-146">`[SubscriptionId <String>]`：訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="c30ab-146">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="c30ab-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="c30ab-147">RELATED LINKS</span></span>

