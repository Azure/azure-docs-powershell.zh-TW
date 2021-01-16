---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubModule.md
ms.openlocfilehash: 44e6451542a75e97a57890261a9a5f312e5ec466
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279396"
---
# <span data-ttu-id="a724c-101">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="a724c-101">Add-AzIotHubModule</span></span>

## <span data-ttu-id="a724c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a724c-102">SYNOPSIS</span></span>
<span data-ttu-id="a724c-103">在 IoT 中樞中的目標 IoT 裝置上建立模組。</span><span class="sxs-lookup"><span data-stu-id="a724c-103">Create a module on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="a724c-104">句法</span><span class="sxs-lookup"><span data-stu-id="a724c-104">SYNTAX</span></span>

### <span data-ttu-id="a724c-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a724c-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a724c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a724c-106">InputObjectSet</span></span>
```
Add-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a724c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a724c-107">ResourceIdSet</span></span>
```
Add-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a724c-108">說明</span><span class="sxs-lookup"><span data-stu-id="a724c-108">DESCRIPTION</span></span>
<span data-ttu-id="a724c-109">在 IoT 中樞中以不同的授權類型在目標 IoT 裝置上建立模組。</span><span class="sxs-lookup"><span data-stu-id="a724c-109">Create a module on a target IoT device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="a724c-110">示例</span><span class="sxs-lookup"><span data-stu-id="a724c-110">EXAMPLES</span></span>

### <span data-ttu-id="a724c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a724c-111">Example 1</span></span>
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

<span data-ttu-id="a724c-112">在目標 IoT 裝置上使用預設授權 (共用私密金鑰) 建立模組。</span><span class="sxs-lookup"><span data-stu-id="a724c-112">Create a module on a target IoT device with default authorization (shared private key).</span></span>

## <span data-ttu-id="a724c-113">參數</span><span class="sxs-lookup"><span data-stu-id="a724c-113">PARAMETERS</span></span>

### <span data-ttu-id="a724c-114">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="a724c-114">-AuthMethod</span></span>
<span data-ttu-id="a724c-115">建立實體的授權類型。</span><span class="sxs-lookup"><span data-stu-id="a724c-115">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="a724c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a724c-116">-DefaultProfile</span></span>
<span data-ttu-id="a724c-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a724c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a724c-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a724c-118">-DeviceId</span></span>
<span data-ttu-id="a724c-119">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="a724c-119">Target Device Id.</span></span>

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

### <span data-ttu-id="a724c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a724c-120">-InputObject</span></span>
<span data-ttu-id="a724c-121">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="a724c-121">IotHub object</span></span>

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

### <span data-ttu-id="a724c-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a724c-122">-IotHubName</span></span>
<span data-ttu-id="a724c-123">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="a724c-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a724c-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="a724c-124">-ModuleId</span></span>
<span data-ttu-id="a724c-125">目的模組識別碼。</span><span class="sxs-lookup"><span data-stu-id="a724c-125">Target Module Id.</span></span>

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

### <span data-ttu-id="a724c-126">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="a724c-126">-PrimaryThumbprint</span></span>
<span data-ttu-id="a724c-127">要用於主鍵的明確的自我簽署憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="a724c-127">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="a724c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a724c-128">-ResourceGroupName</span></span>
<span data-ttu-id="a724c-129">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="a724c-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a724c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a724c-130">-ResourceId</span></span>
<span data-ttu-id="a724c-131">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a724c-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a724c-132">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="a724c-132">-SecondaryThumbprint</span></span>
<span data-ttu-id="a724c-133">用於輔助金鑰的明確的自我簽署憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="a724c-133">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="a724c-134">-確認</span><span class="sxs-lookup"><span data-stu-id="a724c-134">-Confirm</span></span>
<span data-ttu-id="a724c-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a724c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a724c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a724c-136">-WhatIf</span></span>
<span data-ttu-id="a724c-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a724c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a724c-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a724c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a724c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a724c-139">CommonParameters</span></span>
<span data-ttu-id="a724c-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a724c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a724c-141">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a724c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a724c-142">輸入</span><span class="sxs-lookup"><span data-stu-id="a724c-142">INPUTS</span></span>

### <span data-ttu-id="a724c-143">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="a724c-143">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a724c-144">System.object</span><span class="sxs-lookup"><span data-stu-id="a724c-144">System.String</span></span>

## <span data-ttu-id="a724c-145">輸出</span><span class="sxs-lookup"><span data-stu-id="a724c-145">OUTPUTS</span></span>

### <span data-ttu-id="a724c-146">PSModule （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="a724c-146">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

## <span data-ttu-id="a724c-147">筆記</span><span class="sxs-lookup"><span data-stu-id="a724c-147">NOTES</span></span>

## <span data-ttu-id="a724c-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="a724c-148">RELATED LINKS</span></span>