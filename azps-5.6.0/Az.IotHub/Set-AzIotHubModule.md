---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
ms.openlocfilehash: c5e31e1f1fcaf4e889e0b1f3bb85b55a4b0388b0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916942"
---
# <span data-ttu-id="e9f42-101">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="e9f42-101">Set-AzIotHubModule</span></span>

## <span data-ttu-id="e9f42-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e9f42-102">SYNOPSIS</span></span>
<span data-ttu-id="e9f42-103">更新 IoT 中心中目標 IoT 裝置上的模組。</span><span class="sxs-lookup"><span data-stu-id="e9f42-103">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="e9f42-104">語法</span><span class="sxs-lookup"><span data-stu-id="e9f42-104">SYNTAX</span></span>

### <span data-ttu-id="e9f42-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e9f42-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9f42-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e9f42-106">InputObjectSet</span></span>
```
Set-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e9f42-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e9f42-107">ResourceIdSet</span></span>
```
Set-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9f42-108">描述</span><span class="sxs-lookup"><span data-stu-id="e9f42-108">DESCRIPTION</span></span>
<span data-ttu-id="e9f42-109">更新 IoT 中心中目標 IoT 裝置上的模組。</span><span class="sxs-lookup"><span data-stu-id="e9f42-109">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="e9f42-110">例子</span><span class="sxs-lookup"><span data-stu-id="e9f42-110">EXAMPLES</span></span>

### <span data-ttu-id="e9f42-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="e9f42-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -AuthMethod "shared_private_key"

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

<span data-ttu-id="e9f42-112">Iot 裝置模組的更新授權類型。</span><span class="sxs-lookup"><span data-stu-id="e9f42-112">Update authorization type of an Iot device module.</span></span>

## <span data-ttu-id="e9f42-113">參數</span><span class="sxs-lookup"><span data-stu-id="e9f42-113">PARAMETERS</span></span>

### <span data-ttu-id="e9f42-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="e9f42-114">-AuthMethod</span></span>
<span data-ttu-id="e9f42-115">這是要建立實體的授權類型。</span><span class="sxs-lookup"><span data-stu-id="e9f42-115">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="e9f42-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9f42-116">-DefaultProfile</span></span>
<span data-ttu-id="e9f42-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e9f42-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9f42-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e9f42-118">-DeviceId</span></span>
<span data-ttu-id="e9f42-119">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="e9f42-119">Target Device Id.</span></span>

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

### <span data-ttu-id="e9f42-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9f42-120">-InputObject</span></span>
<span data-ttu-id="e9f42-121">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="e9f42-121">IotHub object</span></span>

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

### <span data-ttu-id="e9f42-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e9f42-122">-IotHubName</span></span>
<span data-ttu-id="e9f42-123">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="e9f42-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e9f42-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="e9f42-124">-ModuleId</span></span>
<span data-ttu-id="e9f42-125">目的模組識別碼。</span><span class="sxs-lookup"><span data-stu-id="e9f42-125">Target Module Id.</span></span>

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

### <span data-ttu-id="e9f42-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="e9f42-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="e9f42-127">要用於主鍵的明確自我簽署憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="e9f42-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="e9f42-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9f42-128">-ResourceGroupName</span></span>
<span data-ttu-id="e9f42-129">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="e9f42-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e9f42-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9f42-130">-ResourceId</span></span>
<span data-ttu-id="e9f42-131">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e9f42-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e9f42-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="e9f42-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="e9f42-133">明確自我簽署憑證指紋，以用於次要金鑰。</span><span class="sxs-lookup"><span data-stu-id="e9f42-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="e9f42-134">-確認</span><span class="sxs-lookup"><span data-stu-id="e9f42-134">-Confirm</span></span>
<span data-ttu-id="e9f42-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e9f42-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9f42-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9f42-136">-WhatIf</span></span>
<span data-ttu-id="e9f42-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e9f42-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9f42-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9f42-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9f42-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9f42-139">CommonParameters</span></span>
<span data-ttu-id="e9f42-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e9f42-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9f42-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e9f42-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9f42-142">輸入</span><span class="sxs-lookup"><span data-stu-id="e9f42-142">INPUTS</span></span>

### <span data-ttu-id="e9f42-143">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="e9f42-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e9f42-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e9f42-144">System.String</span></span>

## <span data-ttu-id="e9f42-145">輸出</span><span class="sxs-lookup"><span data-stu-id="e9f42-145">OUTPUTS</span></span>

### <span data-ttu-id="e9f42-146">Microsoft.Azure.Commands.management.IotHub.models.PSModule</span><span class="sxs-lookup"><span data-stu-id="e9f42-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="e9f42-147">筆記</span><span class="sxs-lookup"><span data-stu-id="e9f42-147">NOTES</span></span>

## <span data-ttu-id="e9f42-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9f42-148">RELATED LINKS</span></span>