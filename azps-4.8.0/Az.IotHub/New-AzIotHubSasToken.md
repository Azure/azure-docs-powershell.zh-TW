---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
ms.openlocfilehash: 486ca6543bb32d096e454d16ff3640720f2f53fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969694"
---
# <span data-ttu-id="585ee-101">New-AzIotHubSasToken</span><span class="sxs-lookup"><span data-stu-id="585ee-101">New-AzIotHubSasToken</span></span>

## <span data-ttu-id="585ee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="585ee-102">SYNOPSIS</span></span>
<span data-ttu-id="585ee-103">針對目標 IoT 中樞、device 或 module 產生 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="585ee-103">Generate a SAS token for a target IoT Hub, device or module.</span></span>

## <span data-ttu-id="585ee-104">句法</span><span class="sxs-lookup"><span data-stu-id="585ee-104">SYNTAX</span></span>

### <span data-ttu-id="585ee-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="585ee-105">ResourceSet (Default)</span></span>
```
New-AzIotHubSasToken [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-ModuleId <String>] [-KeyName <String>] [-KeyType <PSKeyType>] [-Duration <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="585ee-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="585ee-106">InputObjectSet</span></span>
```
New-AzIotHubSasToken [-InputObject] <PSIotHub> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="585ee-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="585ee-107">ResourceIdSet</span></span>
```
New-AzIotHubSasToken [-ResourceId] <String> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="585ee-108">說明</span><span class="sxs-lookup"><span data-stu-id="585ee-108">DESCRIPTION</span></span>
<span data-ttu-id="585ee-109">針對裝置 SAS 權杖，原則參數只是用來存取 device registry。</span><span class="sxs-lookup"><span data-stu-id="585ee-109">For device SAS tokens, the policy parameter is used to access the the device registry only.</span></span> <span data-ttu-id="585ee-110">因此，原則應該具備對註冊表的讀取存取權。</span><span class="sxs-lookup"><span data-stu-id="585ee-110">Therefore the policy should have read access to the registry.</span></span>
<span data-ttu-id="585ee-111">針對 IoT 中樞權杖，該原則就是 SA 的一部分。</span><span class="sxs-lookup"><span data-stu-id="585ee-111">For IoT Hub tokens the policy is part of the SAS.</span></span>

## <span data-ttu-id="585ee-112">示例</span><span class="sxs-lookup"><span data-stu-id="585ee-112">EXAMPLES</span></span>

### <span data-ttu-id="585ee-113">範例1</span><span class="sxs-lookup"><span data-stu-id="585ee-113">Example 1</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="585ee-114">使用 iothubowner 原則和主鍵來產生 IoT 中樞 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="585ee-114">Generate an IoT Hub SAS token using the iothubowner policy and primary key.</span></span>

### <span data-ttu-id="585ee-115">範例2</span><span class="sxs-lookup"><span data-stu-id="585ee-115">Example 2</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -KeyName "registryRead" -KeyType "secondary"
```

<span data-ttu-id="585ee-116">使用 registryRead 原則和輔助金鑰來產生 IoT 中樞 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="585ee-116">Generate an IoT Hub SAS token using the registryRead policy and secondary key.</span></span>

### <span data-ttu-id="585ee-117">範例3</span><span class="sxs-lookup"><span data-stu-id="585ee-117">Example 3</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="585ee-118">使用 iothubowner 原則產生裝置 SAS 權杖，以存取 {iothub_name} 裝置註冊。</span><span class="sxs-lookup"><span data-stu-id="585ee-118">Generate a device SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

### <span data-ttu-id="585ee-119">範例4</span><span class="sxs-lookup"><span data-stu-id="585ee-119">Example 4</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="585ee-120">使用 iothubowner 原則產生模組 SAS 權杖，以存取 {iothub_name} 裝置註冊。</span><span class="sxs-lookup"><span data-stu-id="585ee-120">Generate a module SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

## <span data-ttu-id="585ee-121">參數</span><span class="sxs-lookup"><span data-stu-id="585ee-121">PARAMETERS</span></span>

### <span data-ttu-id="585ee-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="585ee-122">-DefaultProfile</span></span>
<span data-ttu-id="585ee-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="585ee-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="585ee-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="585ee-124">-DeviceId</span></span>
<span data-ttu-id="585ee-125">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="585ee-125">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585ee-126">-工期</span><span class="sxs-lookup"><span data-stu-id="585ee-126">-Duration</span></span>
<span data-ttu-id="585ee-127">未來到期 (要產生的權杖) 秒。</span><span class="sxs-lookup"><span data-stu-id="585ee-127">Future expiry (in seconds) of the token to be generated.</span></span>
<span data-ttu-id="585ee-128">預設值為3600。</span><span class="sxs-lookup"><span data-stu-id="585ee-128">Default is 3600.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585ee-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="585ee-129">-InputObject</span></span>
<span data-ttu-id="585ee-130">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="585ee-130">IotHub object</span></span>

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

### <span data-ttu-id="585ee-131">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="585ee-131">-IotHubName</span></span>
<span data-ttu-id="585ee-132">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="585ee-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="585ee-133">-KeyName</span><span class="sxs-lookup"><span data-stu-id="585ee-133">-KeyName</span></span>
<span data-ttu-id="585ee-134">便捷鍵名。</span><span class="sxs-lookup"><span data-stu-id="585ee-134">Access key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585ee-135">-KeyType</span><span class="sxs-lookup"><span data-stu-id="585ee-135">-KeyType</span></span>
<span data-ttu-id="585ee-136">便捷鍵類型。</span><span class="sxs-lookup"><span data-stu-id="585ee-136">Access key type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585ee-137">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="585ee-137">-ModuleId</span></span>
<span data-ttu-id="585ee-138">目的模組識別碼。</span><span class="sxs-lookup"><span data-stu-id="585ee-138">Target Module Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585ee-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="585ee-139">-ResourceGroupName</span></span>
<span data-ttu-id="585ee-140">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="585ee-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="585ee-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="585ee-141">-ResourceId</span></span>
<span data-ttu-id="585ee-142">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="585ee-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="585ee-143">-確認</span><span class="sxs-lookup"><span data-stu-id="585ee-143">-Confirm</span></span>
<span data-ttu-id="585ee-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="585ee-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="585ee-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="585ee-145">-WhatIf</span></span>
<span data-ttu-id="585ee-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="585ee-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="585ee-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="585ee-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="585ee-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="585ee-148">CommonParameters</span></span>
<span data-ttu-id="585ee-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="585ee-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="585ee-150">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="585ee-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="585ee-151">輸入</span><span class="sxs-lookup"><span data-stu-id="585ee-151">INPUTS</span></span>

### <span data-ttu-id="585ee-152">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="585ee-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="585ee-153">System.object</span><span class="sxs-lookup"><span data-stu-id="585ee-153">System.String</span></span>

## <span data-ttu-id="585ee-154">輸出</span><span class="sxs-lookup"><span data-stu-id="585ee-154">OUTPUTS</span></span>

### <span data-ttu-id="585ee-155">System.object</span><span class="sxs-lookup"><span data-stu-id="585ee-155">System.String</span></span>

## <span data-ttu-id="585ee-156">筆記</span><span class="sxs-lookup"><span data-stu-id="585ee-156">NOTES</span></span>

## <span data-ttu-id="585ee-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="585ee-157">RELATED LINKS</span></span>