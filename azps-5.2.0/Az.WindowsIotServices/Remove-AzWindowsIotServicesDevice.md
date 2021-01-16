---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/remove-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 265c0e68dd3f19afbefd8cf993e058f56e3ec9f3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279126"
---
# <span data-ttu-id="92a67-101">Remove-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="92a67-101">Remove-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="92a67-102">摘要</span><span class="sxs-lookup"><span data-stu-id="92a67-102">SYNOPSIS</span></span>
<span data-ttu-id="92a67-103">刪除 Windows IoT 裝置服務。</span><span class="sxs-lookup"><span data-stu-id="92a67-103">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="92a67-104">句法</span><span class="sxs-lookup"><span data-stu-id="92a67-104">SYNTAX</span></span>

### <span data-ttu-id="92a67-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="92a67-105">Delete (Default)</span></span>
```
Remove-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="92a67-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="92a67-106">DeleteViaIdentity</span></span>
```
Remove-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="92a67-107">說明</span><span class="sxs-lookup"><span data-stu-id="92a67-107">DESCRIPTION</span></span>
<span data-ttu-id="92a67-108">刪除 Windows IoT 裝置服務。</span><span class="sxs-lookup"><span data-stu-id="92a67-108">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="92a67-109">示例</span><span class="sxs-lookup"><span data-stu-id="92a67-109">EXAMPLES</span></span>

### <span data-ttu-id="92a67-110">範例1：依名稱移除 Windows IoT 服務</span><span class="sxs-lookup"><span data-stu-id="92a67-110">Example 1: Remove a Windows IoT services by name</span></span>
```powershell
PS C:\> Remove-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test

```

<span data-ttu-id="92a67-111">這個命令會依名稱移除 Windows IoT 服務。</span><span class="sxs-lookup"><span data-stu-id="92a67-111">This command removes a Windows IoT services by name.</span></span>

### <span data-ttu-id="92a67-112">範例2：依管道移除 Windows IoT 服務</span><span class="sxs-lookup"><span data-stu-id="92a67-112">Example 2: Remove a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01 | Remove-AzWindowsIotServicesDevice


```

<span data-ttu-id="92a67-113">這個命令會依管道移除 Windows IoT 服務。</span><span class="sxs-lookup"><span data-stu-id="92a67-113">This command removes a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="92a67-114">參數</span><span class="sxs-lookup"><span data-stu-id="92a67-114">PARAMETERS</span></span>

### <span data-ttu-id="92a67-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92a67-115">-DefaultProfile</span></span>
<span data-ttu-id="92a67-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="92a67-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92a67-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92a67-117">-InputObject</span></span>
<span data-ttu-id="92a67-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="92a67-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="92a67-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="92a67-119">-Name</span></span>
<span data-ttu-id="92a67-120">Windows IoT 裝置服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="92a67-120">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="92a67-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92a67-121">-ResourceGroupName</span></span>
<span data-ttu-id="92a67-122">包含 Windows IoT 裝置服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="92a67-122">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="92a67-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92a67-123">-SubscriptionId</span></span>
<span data-ttu-id="92a67-124">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="92a67-124">The subscription identifier.</span></span>

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

### <span data-ttu-id="92a67-125">-確認</span><span class="sxs-lookup"><span data-stu-id="92a67-125">-Confirm</span></span>
<span data-ttu-id="92a67-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="92a67-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92a67-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92a67-127">-WhatIf</span></span>
<span data-ttu-id="92a67-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="92a67-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92a67-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92a67-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92a67-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92a67-130">CommonParameters</span></span>
<span data-ttu-id="92a67-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="92a67-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92a67-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="92a67-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92a67-133">輸入</span><span class="sxs-lookup"><span data-stu-id="92a67-133">INPUTS</span></span>

### <span data-ttu-id="92a67-134">IWindowsIotServicesIdentity （WindowsIotServices）的</span><span class="sxs-lookup"><span data-stu-id="92a67-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="92a67-135">輸出</span><span class="sxs-lookup"><span data-stu-id="92a67-135">OUTPUTS</span></span>

### <span data-ttu-id="92a67-136">IDeviceService （WindowsIotServices）。 Api20190601。</span><span class="sxs-lookup"><span data-stu-id="92a67-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="92a67-137">筆記</span><span class="sxs-lookup"><span data-stu-id="92a67-137">NOTES</span></span>

<span data-ttu-id="92a67-138">別名</span><span class="sxs-lookup"><span data-stu-id="92a67-138">ALIASES</span></span>

<span data-ttu-id="92a67-139">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="92a67-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="92a67-140">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="92a67-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="92a67-141">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="92a67-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="92a67-142">INPUTOBJECT <IWindowsIotServicesIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="92a67-142">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="92a67-143">`[DeviceName <String>]`： Windows IoT 裝置服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="92a67-143">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="92a67-144">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="92a67-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="92a67-145">`[ResourceGroupName <String>]`：包含 Windows IoT 裝置服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="92a67-145">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="92a67-146">`[SubscriptionId <String>]`：訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="92a67-146">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="92a67-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="92a67-147">RELATED LINKS</span></span>

