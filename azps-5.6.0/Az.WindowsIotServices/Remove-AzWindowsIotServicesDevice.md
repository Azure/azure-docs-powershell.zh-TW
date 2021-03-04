---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/powershell/module/az.windowsiotservices/remove-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Remove-AzWindowsIotServicesDevice.md
ms.openlocfilehash: e0012bab0679a49e0ad5a117845ca9e0e5d5a6db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906821"
---
# <span data-ttu-id="f20fb-101">Remove-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="f20fb-101">Remove-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="f20fb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f20fb-102">SYNOPSIS</span></span>
<span data-ttu-id="f20fb-103">刪除 Windows IoT 裝置服務。</span><span class="sxs-lookup"><span data-stu-id="f20fb-103">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="f20fb-104">語法</span><span class="sxs-lookup"><span data-stu-id="f20fb-104">SYNTAX</span></span>

### <span data-ttu-id="f20fb-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="f20fb-105">Delete (Default)</span></span>
```
Remove-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f20fb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f20fb-106">DeleteViaIdentity</span></span>
```
Remove-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f20fb-107">描述</span><span class="sxs-lookup"><span data-stu-id="f20fb-107">DESCRIPTION</span></span>
<span data-ttu-id="f20fb-108">刪除 Windows IoT 裝置服務。</span><span class="sxs-lookup"><span data-stu-id="f20fb-108">Delete a Windows IoT Device Service.</span></span>

## <span data-ttu-id="f20fb-109">例子</span><span class="sxs-lookup"><span data-stu-id="f20fb-109">EXAMPLES</span></span>

### <span data-ttu-id="f20fb-110">範例 1：根據名稱移除 Windows IoT 服務</span><span class="sxs-lookup"><span data-stu-id="f20fb-110">Example 1: Remove a Windows IoT services by name</span></span>
```powershell
PS C:\> Remove-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test

```

<span data-ttu-id="f20fb-111">此命令會按名稱移除 Windows IoT 服務。</span><span class="sxs-lookup"><span data-stu-id="f20fb-111">This command removes a Windows IoT services by name.</span></span>

### <span data-ttu-id="f20fb-112">範例 2：根據管線移除 Windows IoT 服務</span><span class="sxs-lookup"><span data-stu-id="f20fb-112">Example 2: Remove a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01 | Remove-AzWindowsIotServicesDevice


```

<span data-ttu-id="f20fb-113">此命令會按管線移除 Windows IoT 服務。</span><span class="sxs-lookup"><span data-stu-id="f20fb-113">This command removes a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="f20fb-114">參數</span><span class="sxs-lookup"><span data-stu-id="f20fb-114">PARAMETERS</span></span>

### <span data-ttu-id="f20fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f20fb-115">-DefaultProfile</span></span>
<span data-ttu-id="f20fb-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f20fb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f20fb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f20fb-117">-InputObject</span></span>
<span data-ttu-id="f20fb-118">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f20fb-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f20fb-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f20fb-119">-Name</span></span>
<span data-ttu-id="f20fb-120">Windows IoT 裝置服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="f20fb-120">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="f20fb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f20fb-121">-ResourceGroupName</span></span>
<span data-ttu-id="f20fb-122">包含 Windows IoT 裝置服務的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f20fb-122">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="f20fb-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f20fb-123">-SubscriptionId</span></span>
<span data-ttu-id="f20fb-124">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="f20fb-124">The subscription identifier.</span></span>

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

### <span data-ttu-id="f20fb-125">-確認</span><span class="sxs-lookup"><span data-stu-id="f20fb-125">-Confirm</span></span>
<span data-ttu-id="f20fb-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f20fb-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f20fb-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f20fb-127">-WhatIf</span></span>
<span data-ttu-id="f20fb-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f20fb-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f20fb-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f20fb-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f20fb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f20fb-130">CommonParameters</span></span>
<span data-ttu-id="f20fb-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f20fb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f20fb-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f20fb-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f20fb-133">輸入</span><span class="sxs-lookup"><span data-stu-id="f20fb-133">INPUTS</span></span>

### <span data-ttu-id="f20fb-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="f20fb-134">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="f20fb-135">輸出</span><span class="sxs-lookup"><span data-stu-id="f20fb-135">OUTPUTS</span></span>

### <span data-ttu-id="f20fb-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="f20fb-136">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="f20fb-137">筆記</span><span class="sxs-lookup"><span data-stu-id="f20fb-137">NOTES</span></span>

<span data-ttu-id="f20fb-138">別名</span><span class="sxs-lookup"><span data-stu-id="f20fb-138">ALIASES</span></span>

<span data-ttu-id="f20fb-139">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f20fb-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f20fb-140">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f20fb-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f20fb-141">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f20fb-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f20fb-142">INPUTOBJECT： <IWindowsIotServicesIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f20fb-142">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f20fb-143">`[DeviceName <String>]`：Windows IoT 裝置服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="f20fb-143">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="f20fb-144">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="f20fb-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f20fb-145">`[ResourceGroupName <String>]`：包含 Windows IoT 裝置服務的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f20fb-145">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="f20fb-146">`[SubscriptionId <String>]`：訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="f20fb-146">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="f20fb-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="f20fb-147">RELATED LINKS</span></span>

