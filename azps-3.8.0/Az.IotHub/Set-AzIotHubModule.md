---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubModule.md
ms.openlocfilehash: c88ee9af5d03b50ed80bf677ccff6e7236668756
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957339"
---
# <span data-ttu-id="e3308-101">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="e3308-101">Set-AzIotHubModule</span></span>

## <span data-ttu-id="e3308-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3308-102">SYNOPSIS</span></span>
<span data-ttu-id="e3308-103">在 IoT 中樞中更新目標 IoT 裝置上的模組。</span><span class="sxs-lookup"><span data-stu-id="e3308-103">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="e3308-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3308-104">SYNTAX</span></span>

### <span data-ttu-id="e3308-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e3308-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3308-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e3308-106">InputObjectSet</span></span>
```
Set-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3308-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e3308-107">ResourceIdSet</span></span>
```
Set-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3308-108">說明</span><span class="sxs-lookup"><span data-stu-id="e3308-108">DESCRIPTION</span></span>
<span data-ttu-id="e3308-109">在 IoT 中樞中更新目標 IoT 裝置上的模組。</span><span class="sxs-lookup"><span data-stu-id="e3308-109">Update a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="e3308-110">示例</span><span class="sxs-lookup"><span data-stu-id="e3308-110">EXAMPLES</span></span>

### <span data-ttu-id="e3308-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e3308-111">Example 1</span></span>
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

<span data-ttu-id="e3308-112">更新 Iot 裝置模組的授權類型。</span><span class="sxs-lookup"><span data-stu-id="e3308-112">Update authorization type of an Iot device module.</span></span>

## <span data-ttu-id="e3308-113">參數</span><span class="sxs-lookup"><span data-stu-id="e3308-113">PARAMETERS</span></span>

### <span data-ttu-id="e3308-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="e3308-114">-AuthMethod</span></span>
<span data-ttu-id="e3308-115">建立實體的授權類型。</span><span class="sxs-lookup"><span data-stu-id="e3308-115">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="e3308-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3308-116">-DefaultProfile</span></span>
<span data-ttu-id="e3308-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3308-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3308-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="e3308-118">-DeviceId</span></span>
<span data-ttu-id="e3308-119">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3308-119">Target Device Id.</span></span>

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

### <span data-ttu-id="e3308-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3308-120">-InputObject</span></span>
<span data-ttu-id="e3308-121">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="e3308-121">IotHub object</span></span>

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

### <span data-ttu-id="e3308-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="e3308-122">-IotHubName</span></span>
<span data-ttu-id="e3308-123">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="e3308-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="e3308-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="e3308-124">-ModuleId</span></span>
<span data-ttu-id="e3308-125">目的模組識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3308-125">Target Module Id.</span></span>

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

### <span data-ttu-id="e3308-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="e3308-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="e3308-127">要用於主鍵的明確的自我簽署憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="e3308-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="e3308-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3308-128">-ResourceGroupName</span></span>
<span data-ttu-id="e3308-129">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="e3308-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e3308-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3308-130">-ResourceId</span></span>
<span data-ttu-id="e3308-131">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e3308-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e3308-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="e3308-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="e3308-133">用於輔助金鑰的明確的自我簽署憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="e3308-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="e3308-134">-確認</span><span class="sxs-lookup"><span data-stu-id="e3308-134">-Confirm</span></span>
<span data-ttu-id="e3308-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e3308-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3308-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3308-136">-WhatIf</span></span>
<span data-ttu-id="e3308-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e3308-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3308-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3308-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3308-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3308-139">CommonParameters</span></span>
<span data-ttu-id="e3308-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3308-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3308-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3308-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3308-142">輸入</span><span class="sxs-lookup"><span data-stu-id="e3308-142">INPUTS</span></span>

### <span data-ttu-id="e3308-143">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="e3308-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="e3308-144">System.object</span><span class="sxs-lookup"><span data-stu-id="e3308-144">System.String</span></span>

## <span data-ttu-id="e3308-145">輸出</span><span class="sxs-lookup"><span data-stu-id="e3308-145">OUTPUTS</span></span>

### <span data-ttu-id="e3308-146">PSModule （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="e3308-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="e3308-147">筆記</span><span class="sxs-lookup"><span data-stu-id="e3308-147">NOTES</span></span>

## <span data-ttu-id="e3308-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3308-148">RELATED LINKS</span></span>