---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
ms.openlocfilehash: 09a4201d8add325c068358615a48a86c5e60911a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913858"
---
# <span data-ttu-id="c380b-101">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="c380b-101">Add-AzIotHubModule</span></span>

## <span data-ttu-id="c380b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c380b-102">SYNOPSIS</span></span>
<span data-ttu-id="c380b-103">在 IoT 中心的目標 IoT 裝置上建立模組。</span><span class="sxs-lookup"><span data-stu-id="c380b-103">Create a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="c380b-104">語法</span><span class="sxs-lookup"><span data-stu-id="c380b-104">SYNTAX</span></span>

### <span data-ttu-id="c380b-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c380b-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c380b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c380b-106">InputObjectSet</span></span>
```
Add-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c380b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c380b-107">ResourceIdSet</span></span>
```
Add-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c380b-108">描述</span><span class="sxs-lookup"><span data-stu-id="c380b-108">DESCRIPTION</span></span>
<span data-ttu-id="c380b-109">在 IoT 中心的授權類型不同的目標 IoT 裝置上建立模組。</span><span class="sxs-lookup"><span data-stu-id="c380b-109">Create a module on a target IoT device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="c380b-110">例子</span><span class="sxs-lookup"><span data-stu-id="c380b-110">EXAMPLES</span></span>

### <span data-ttu-id="c380b-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="c380b-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -AuthMethod shared_private_key

ModuleId                   : myModule1
DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
ManagedBy                  : 
```

<span data-ttu-id="c380b-112">在具有預設授權的目標 IoT 裝置上建立模組， (共用私密金鑰) 。</span><span class="sxs-lookup"><span data-stu-id="c380b-112">Create a module on a target IoT device with default authorization (shared private key).</span></span>

## <span data-ttu-id="c380b-113">參數</span><span class="sxs-lookup"><span data-stu-id="c380b-113">PARAMETERS</span></span>

### <span data-ttu-id="c380b-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="c380b-114">-AuthMethod</span></span>
<span data-ttu-id="c380b-115">這是要建立實體的授權類型。</span><span class="sxs-lookup"><span data-stu-id="c380b-115">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: (All)
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c380b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c380b-116">-DefaultProfile</span></span>
<span data-ttu-id="c380b-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c380b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c380b-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="c380b-118">-DeviceId</span></span>
<span data-ttu-id="c380b-119">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="c380b-119">Target Device Id.</span></span>

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

### <span data-ttu-id="c380b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c380b-120">-InputObject</span></span>
<span data-ttu-id="c380b-121">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="c380b-121">IotHub object</span></span>

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

### <span data-ttu-id="c380b-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c380b-122">-IotHubName</span></span>
<span data-ttu-id="c380b-123">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="c380b-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c380b-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="c380b-124">-ModuleId</span></span>
<span data-ttu-id="c380b-125">目的模組識別碼。</span><span class="sxs-lookup"><span data-stu-id="c380b-125">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c380b-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="c380b-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="c380b-127">要用於主鍵的明確自我簽署憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="c380b-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c380b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c380b-128">-ResourceGroupName</span></span>
<span data-ttu-id="c380b-129">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="c380b-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c380b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c380b-130">-ResourceId</span></span>
<span data-ttu-id="c380b-131">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c380b-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c380b-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="c380b-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="c380b-133">明確自我簽署憑證指紋，以用於次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="c380b-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type:System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c380b-134">-確認</span><span class="sxs-lookup"><span data-stu-id="c380b-134">-Confirm</span></span>
<span data-ttu-id="c380b-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c380b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c380b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c380b-136">-WhatIf</span></span>
<span data-ttu-id="c380b-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c380b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c380b-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c380b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c380b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c380b-139">CommonParameters</span></span>
<span data-ttu-id="c380b-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c380b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c380b-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c380b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c380b-142">輸入</span><span class="sxs-lookup"><span data-stu-id="c380b-142">INPUTS</span></span>

### <span data-ttu-id="c380b-143">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c380b-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c380b-144">System.String</span><span class="sxs-lookup"><span data-stu-id="c380b-144">System.String</span></span>

## <span data-ttu-id="c380b-145">輸出</span><span class="sxs-lookup"><span data-stu-id="c380b-145">OUTPUTS</span></span>

### <span data-ttu-id="c380b-146">Microsoft.Azure.Commands.management.IotHub.models.PSModule</span><span class="sxs-lookup"><span data-stu-id="c380b-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="c380b-147">筆記</span><span class="sxs-lookup"><span data-stu-id="c380b-147">NOTES</span></span>

## <span data-ttu-id="c380b-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="c380b-148">RELATED LINKS</span></span>