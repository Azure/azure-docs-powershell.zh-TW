---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
ms.openlocfilehash: 8d22b5923b59ef5807419fac4486cd64d5d2b86e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969681"
---
# <span data-ttu-id="c56c3-101">Remove-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="c56c3-101">Remove-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="c56c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c56c3-102">SYNOPSIS</span></span>
<span data-ttu-id="c56c3-103">從指定的邊緣裝置將非邊緣裝置移除為子級。</span><span class="sxs-lookup"><span data-stu-id="c56c3-103">Remove non edge devices as children from specified edge device.</span></span>

## <span data-ttu-id="c56c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="c56c3-104">SYNTAX</span></span>

### <span data-ttu-id="c56c3-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c56c3-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c56c3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c56c3-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c56c3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c56c3-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c56c3-108">說明</span><span class="sxs-lookup"><span data-stu-id="c56c3-108">DESCRIPTION</span></span>
<span data-ttu-id="c56c3-109">移除所有或提到的非邊緣裝置，做為指定為「edge」裝置的子系。</span><span class="sxs-lookup"><span data-stu-id="c56c3-109">Remove all or mentioned non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="c56c3-110">示例</span><span class="sxs-lookup"><span data-stu-id="c56c3-110">EXAMPLES</span></span>

### <span data-ttu-id="c56c3-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c56c3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2 -Passthru

True
```

<span data-ttu-id="c56c3-112">將提及的裝置移除為指定裝置的子系。</span><span class="sxs-lookup"><span data-stu-id="c56c3-112">Remove mentioned devices as children of specified device.</span></span>

### <span data-ttu-id="c56c3-113">範例2</span><span class="sxs-lookup"><span data-stu-id="c56c3-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Passthru

True
```

<span data-ttu-id="c56c3-114">將所有非邊緣裝置移除為指定為「edge」裝置的子系。</span><span class="sxs-lookup"><span data-stu-id="c56c3-114">Remove all non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="c56c3-115">參數</span><span class="sxs-lookup"><span data-stu-id="c56c3-115">PARAMETERS</span></span>

### <span data-ttu-id="c56c3-116">-兒童</span><span class="sxs-lookup"><span data-stu-id="c56c3-116">-Children</span></span>
<span data-ttu-id="c56c3-117">子裝置清單 (逗號分隔) 只包含非邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="c56c3-117">Child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c56c3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c56c3-118">-DefaultProfile</span></span>
<span data-ttu-id="c56c3-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c56c3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c56c3-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="c56c3-120">-DeviceId</span></span>
<span data-ttu-id="c56c3-121">Edge 裝置的 Id。</span><span class="sxs-lookup"><span data-stu-id="c56c3-121">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c56c3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c56c3-122">-InputObject</span></span>
<span data-ttu-id="c56c3-123">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="c56c3-123">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c56c3-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c56c3-124">-IotHubName</span></span>
<span data-ttu-id="c56c3-125">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="c56c3-125">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c56c3-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c56c3-126">-PassThru</span></span>
<span data-ttu-id="c56c3-127">允許傳回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="c56c3-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="c56c3-128">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="c56c3-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c56c3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c56c3-129">-ResourceGroupName</span></span>
<span data-ttu-id="c56c3-130">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="c56c3-130">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c56c3-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c56c3-131">-ResourceId</span></span>
<span data-ttu-id="c56c3-132">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c56c3-132">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c56c3-133">-確認</span><span class="sxs-lookup"><span data-stu-id="c56c3-133">-Confirm</span></span>
<span data-ttu-id="c56c3-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c56c3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c56c3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c56c3-135">-WhatIf</span></span>
<span data-ttu-id="c56c3-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c56c3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c56c3-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c56c3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c56c3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c56c3-138">CommonParameters</span></span>
<span data-ttu-id="c56c3-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c56c3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c56c3-140">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c56c3-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c56c3-141">輸入</span><span class="sxs-lookup"><span data-stu-id="c56c3-141">INPUTS</span></span>

### <span data-ttu-id="c56c3-142">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="c56c3-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c56c3-143">System.object</span><span class="sxs-lookup"><span data-stu-id="c56c3-143">System.String</span></span>

## <span data-ttu-id="c56c3-144">輸出</span><span class="sxs-lookup"><span data-stu-id="c56c3-144">OUTPUTS</span></span>

### <span data-ttu-id="c56c3-145">System.object</span><span class="sxs-lookup"><span data-stu-id="c56c3-145">System.Boolean</span></span>

## <span data-ttu-id="c56c3-146">筆記</span><span class="sxs-lookup"><span data-stu-id="c56c3-146">NOTES</span></span>

## <span data-ttu-id="c56c3-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="c56c3-147">RELATED LINKS</span></span>