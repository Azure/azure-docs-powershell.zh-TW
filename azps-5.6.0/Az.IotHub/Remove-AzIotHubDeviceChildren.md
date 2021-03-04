---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
ms.openlocfilehash: 296793309dbcae7317353e41f9f3562a020c9be2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917174"
---
# <span data-ttu-id="15959-101">Remove-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="15959-101">Remove-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="15959-102">簡介</span><span class="sxs-lookup"><span data-stu-id="15959-102">SYNOPSIS</span></span>
<span data-ttu-id="15959-103">將非邊緣裝置從指定的邊緣裝置移除為子女。</span><span class="sxs-lookup"><span data-stu-id="15959-103">Remove non edge devices as children from specified edge device.</span></span>

## <span data-ttu-id="15959-104">語法</span><span class="sxs-lookup"><span data-stu-id="15959-104">SYNTAX</span></span>

### <span data-ttu-id="15959-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="15959-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="15959-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="15959-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15959-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="15959-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15959-108">描述</span><span class="sxs-lookup"><span data-stu-id="15959-108">DESCRIPTION</span></span>
<span data-ttu-id="15959-109">移除所有或提及的非邊緣裝置為兒童指定的邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="15959-109">Remove all or mentioned non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="15959-110">例子</span><span class="sxs-lookup"><span data-stu-id="15959-110">EXAMPLES</span></span>

### <span data-ttu-id="15959-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="15959-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2 -Passthru

True
```

<span data-ttu-id="15959-112">將提及的裝置移除為指定裝置的孩子。</span><span class="sxs-lookup"><span data-stu-id="15959-112">Remove mentioned devices as children of specified device.</span></span>

### <span data-ttu-id="15959-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="15959-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Passthru

True
```

<span data-ttu-id="15959-114">移除所有非邊緣裝置做為兒童指定的邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="15959-114">Remove all non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="15959-115">參數</span><span class="sxs-lookup"><span data-stu-id="15959-115">PARAMETERS</span></span>

### <span data-ttu-id="15959-116">-兒童</span><span class="sxs-lookup"><span data-stu-id="15959-116">-Children</span></span>
<span data-ttu-id="15959-117">子裝置清單 (逗號分隔) 只包含非邊緣裝置。</span><span class="sxs-lookup"><span data-stu-id="15959-117">Child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="15959-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15959-118">-DefaultProfile</span></span>
<span data-ttu-id="15959-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="15959-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15959-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="15959-120">-DeviceId</span></span>
<span data-ttu-id="15959-121">邊緣裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="15959-121">Id of edge device.</span></span>

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

### <span data-ttu-id="15959-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15959-122">-InputObject</span></span>
<span data-ttu-id="15959-123">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="15959-123">IotHub object</span></span>

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

### <span data-ttu-id="15959-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="15959-124">-IotHubName</span></span>
<span data-ttu-id="15959-125">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="15959-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="15959-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15959-126">-PassThru</span></span>
<span data-ttu-id="15959-127">允許返回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="15959-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="15959-128">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="15959-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="15959-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15959-129">-ResourceGroupName</span></span>
<span data-ttu-id="15959-130">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="15959-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="15959-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15959-131">-ResourceId</span></span>
<span data-ttu-id="15959-132">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="15959-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="15959-133">-確認</span><span class="sxs-lookup"><span data-stu-id="15959-133">-Confirm</span></span>
<span data-ttu-id="15959-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="15959-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15959-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15959-135">-WhatIf</span></span>
<span data-ttu-id="15959-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="15959-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15959-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="15959-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15959-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15959-138">CommonParameters</span></span>
<span data-ttu-id="15959-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="15959-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15959-140">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="15959-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15959-141">輸入</span><span class="sxs-lookup"><span data-stu-id="15959-141">INPUTS</span></span>

### <span data-ttu-id="15959-142">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="15959-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="15959-143">System.String</span><span class="sxs-lookup"><span data-stu-id="15959-143">System.String</span></span>

## <span data-ttu-id="15959-144">輸出</span><span class="sxs-lookup"><span data-stu-id="15959-144">OUTPUTS</span></span>

### <span data-ttu-id="15959-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="15959-145">System.Boolean</span></span>

## <span data-ttu-id="15959-146">筆記</span><span class="sxs-lookup"><span data-stu-id="15959-146">NOTES</span></span>

## <span data-ttu-id="15959-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="15959-147">RELATED LINKS</span></span>
