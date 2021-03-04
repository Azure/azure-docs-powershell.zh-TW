---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothubsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubSasToken.md
ms.openlocfilehash: 39b936f6b9ec4bb133ecc6510963207c5e7d96a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908182"
---
# <span data-ttu-id="c8959-101">New-AzIotHubSasToken</span><span class="sxs-lookup"><span data-stu-id="c8959-101">New-AzIotHubSasToken</span></span>

## <span data-ttu-id="c8959-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c8959-102">SYNOPSIS</span></span>
<span data-ttu-id="c8959-103">產生目標 IoT 中樞、裝置或模組的 SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="c8959-103">Generate a SAS token for a target IoT Hub, device or module.</span></span>

## <span data-ttu-id="c8959-104">語法</span><span class="sxs-lookup"><span data-stu-id="c8959-104">SYNTAX</span></span>

### <span data-ttu-id="c8959-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c8959-105">ResourceSet (Default)</span></span>
```
New-AzIotHubSasToken [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-ModuleId <String>] [-KeyName <String>] [-KeyType <PSKeyType>] [-Duration <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8959-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c8959-106">InputObjectSet</span></span>
```
New-AzIotHubSasToken [-InputObject] <PSIotHub> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8959-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c8959-107">ResourceIdSet</span></span>
```
New-AzIotHubSasToken [-ResourceId] <String> [-DeviceId <String>] [-ModuleId <String>] [-KeyName <String>]
 [-KeyType <PSKeyType>] [-Duration <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8959-108">描述</span><span class="sxs-lookup"><span data-stu-id="c8959-108">DESCRIPTION</span></span>
<span data-ttu-id="c8959-109">針對裝置 SAS 權杖，策略參數只會用來存取裝置註冊表。</span><span class="sxs-lookup"><span data-stu-id="c8959-109">For device SAS tokens, the policy parameter is used to access the the device registry only.</span></span> <span data-ttu-id="c8959-110">因此，該策略應該具有對註冊表的讀取存取權。</span><span class="sxs-lookup"><span data-stu-id="c8959-110">Therefore the policy should have read access to the registry.</span></span>
<span data-ttu-id="c8959-111">針對 IoT 中樞權杖，該策略是 SAS 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c8959-111">For IoT Hub tokens the policy is part of the SAS.</span></span>

## <span data-ttu-id="c8959-112">例子</span><span class="sxs-lookup"><span data-stu-id="c8959-112">EXAMPLES</span></span>

### <span data-ttu-id="c8959-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="c8959-113">Example 1</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="c8959-114">使用 iothubowner 策略和主鍵產生 IoT Hub SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="c8959-114">Generate an IoT Hub SAS token using the iothubowner policy and primary key.</span></span>

### <span data-ttu-id="c8959-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="c8959-115">Example 2</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -KeyName "registryRead" -KeyType "secondary"
```

<span data-ttu-id="c8959-116">使用 registryRead 策略和次要機碼產生 IoT Hub SAS 權杖。</span><span class="sxs-lookup"><span data-stu-id="c8959-116">Generate an IoT Hub SAS token using the registryRead policy and secondary key.</span></span>

### <span data-ttu-id="c8959-117">範例 3</span><span class="sxs-lookup"><span data-stu-id="c8959-117">Example 3</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="c8959-118">使用 iothubowner 策略產生裝置 SAS 權杖，以存取 {iothub_name} 裝置註冊表。</span><span class="sxs-lookup"><span data-stu-id="c8959-118">Generate a device SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

### <span data-ttu-id="c8959-119">範例 4</span><span class="sxs-lookup"><span data-stu-id="c8959-119">Example 4</span></span>
```powershell
PS C:\> New-AzIotHubSasToken -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="c8959-120">使用 iothubowner 策略產生模組 SAS 權杖，以存取 {iothub_name} 裝置註冊表。</span><span class="sxs-lookup"><span data-stu-id="c8959-120">Generate a module SAS token using the iothubowner policy to access the {iothub_name} device registry.</span></span>

## <span data-ttu-id="c8959-121">參數</span><span class="sxs-lookup"><span data-stu-id="c8959-121">PARAMETERS</span></span>

### <span data-ttu-id="c8959-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8959-122">-DefaultProfile</span></span>
<span data-ttu-id="c8959-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8959-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8959-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="c8959-124">-DeviceId</span></span>
<span data-ttu-id="c8959-125">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="c8959-125">Target Device Id.</span></span>

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

### <span data-ttu-id="c8959-126">-工期</span><span class="sxs-lookup"><span data-stu-id="c8959-126">-Duration</span></span>
<span data-ttu-id="c8959-127">未來到期 (，) 產生權杖的秒數。</span><span class="sxs-lookup"><span data-stu-id="c8959-127">Future expiry (in seconds) of the token to be generated.</span></span>
<span data-ttu-id="c8959-128">預設值為 3600。</span><span class="sxs-lookup"><span data-stu-id="c8959-128">Default is 3600.</span></span>

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

### <span data-ttu-id="c8959-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8959-129">-InputObject</span></span>
<span data-ttu-id="c8959-130">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="c8959-130">IotHub object</span></span>

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

### <span data-ttu-id="c8959-131">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c8959-131">-IotHubName</span></span>
<span data-ttu-id="c8959-132">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="c8959-132">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c8959-133">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c8959-133">-KeyName</span></span>
<span data-ttu-id="c8959-134">Access 鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="c8959-134">Access key name.</span></span>

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

### <span data-ttu-id="c8959-135">-KeyType</span><span class="sxs-lookup"><span data-stu-id="c8959-135">-KeyType</span></span>
<span data-ttu-id="c8959-136">Access 鍵類型。</span><span class="sxs-lookup"><span data-stu-id="c8959-136">Access key type.</span></span>

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

### <span data-ttu-id="c8959-137">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="c8959-137">-ModuleId</span></span>
<span data-ttu-id="c8959-138">目的模組識別碼。</span><span class="sxs-lookup"><span data-stu-id="c8959-138">Target Module Id.</span></span>

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

### <span data-ttu-id="c8959-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8959-139">-ResourceGroupName</span></span>
<span data-ttu-id="c8959-140">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="c8959-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c8959-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8959-141">-ResourceId</span></span>
<span data-ttu-id="c8959-142">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c8959-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c8959-143">-確認</span><span class="sxs-lookup"><span data-stu-id="c8959-143">-Confirm</span></span>
<span data-ttu-id="c8959-144">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c8959-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8959-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8959-145">-WhatIf</span></span>
<span data-ttu-id="c8959-146">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c8959-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8959-147">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c8959-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8959-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8959-148">CommonParameters</span></span>
<span data-ttu-id="c8959-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c8959-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8959-150">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c8959-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8959-151">輸入</span><span class="sxs-lookup"><span data-stu-id="c8959-151">INPUTS</span></span>

### <span data-ttu-id="c8959-152">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c8959-152">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c8959-153">System.String</span><span class="sxs-lookup"><span data-stu-id="c8959-153">System.String</span></span>

## <span data-ttu-id="c8959-154">輸出</span><span class="sxs-lookup"><span data-stu-id="c8959-154">OUTPUTS</span></span>

### <span data-ttu-id="c8959-155">System.String</span><span class="sxs-lookup"><span data-stu-id="c8959-155">System.String</span></span>

## <span data-ttu-id="c8959-156">筆記</span><span class="sxs-lookup"><span data-stu-id="c8959-156">NOTES</span></span>

## <span data-ttu-id="c8959-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8959-157">RELATED LINKS</span></span>
