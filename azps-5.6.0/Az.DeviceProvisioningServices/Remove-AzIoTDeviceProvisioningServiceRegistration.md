---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: f72aa2ab648de33baaf50e181afa98e12ac921a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910233"
---
# <span data-ttu-id="b6b90-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="b6b90-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="b6b90-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b6b90-102">SYNOPSIS</span></span>
<span data-ttu-id="b6b90-103">刪除裝置註冊。</span><span class="sxs-lookup"><span data-stu-id="b6b90-103">Deletes the device registration.</span></span>

## <span data-ttu-id="b6b90-104">語法</span><span class="sxs-lookup"><span data-stu-id="b6b90-104">SYNTAX</span></span>

### <span data-ttu-id="b6b90-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b6b90-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6b90-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b6b90-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b6b90-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b6b90-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> -RegistrationId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6b90-108">描述</span><span class="sxs-lookup"><span data-stu-id="b6b90-108">DESCRIPTION</span></span>
<span data-ttu-id="b6b90-109">刪除 Azure IoT Hub 裝置設置服務中的裝置註冊。</span><span class="sxs-lookup"><span data-stu-id="b6b90-109">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="b6b90-110">例子</span><span class="sxs-lookup"><span data-stu-id="b6b90-110">EXAMPLES</span></span>

### <span data-ttu-id="b6b90-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="b6b90-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="b6b90-112">刪除 Azure IoT Hub 裝置設置服務中的裝置註冊。</span><span class="sxs-lookup"><span data-stu-id="b6b90-112">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="b6b90-113">參數</span><span class="sxs-lookup"><span data-stu-id="b6b90-113">PARAMETERS</span></span>

### <span data-ttu-id="b6b90-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6b90-114">-DefaultProfile</span></span>
<span data-ttu-id="b6b90-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6b90-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6b90-116">-DpsName</span><span class="sxs-lookup"><span data-stu-id="b6b90-116">-DpsName</span></span>
<span data-ttu-id="b6b90-117">IoT 裝置設置服務的名稱</span><span class="sxs-lookup"><span data-stu-id="b6b90-117">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="b6b90-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="b6b90-118">-DpsObject</span></span>
<span data-ttu-id="b6b90-119">IoT 裝置設置服務物件</span><span class="sxs-lookup"><span data-stu-id="b6b90-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6b90-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6b90-120">-PassThru</span></span>
<span data-ttu-id="b6b90-121">允許返回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="b6b90-121">Allows to return the boolean object.</span></span>
<span data-ttu-id="b6b90-122">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b6b90-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b6b90-123">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="b6b90-123">-RegistrationId</span></span>
<span data-ttu-id="b6b90-124">裝置註冊的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b6b90-124">ID of device registration.</span></span>

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

### <span data-ttu-id="b6b90-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6b90-125">-ResourceGroupName</span></span>
<span data-ttu-id="b6b90-126">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="b6b90-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b6b90-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6b90-127">-ResourceId</span></span>
<span data-ttu-id="b6b90-128">IoT 裝置資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b6b90-128">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="b6b90-129">-確認</span><span class="sxs-lookup"><span data-stu-id="b6b90-129">-Confirm</span></span>
<span data-ttu-id="b6b90-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b6b90-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6b90-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6b90-131">-WhatIf</span></span>
<span data-ttu-id="b6b90-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b6b90-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6b90-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b6b90-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6b90-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6b90-134">CommonParameters</span></span>
<span data-ttu-id="b6b90-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b6b90-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6b90-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b6b90-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6b90-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b6b90-137">INPUTS</span></span>

### <span data-ttu-id="b6b90-138">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="b6b90-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="b6b90-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b6b90-139">System.String</span></span>

## <span data-ttu-id="b6b90-140">輸出</span><span class="sxs-lookup"><span data-stu-id="b6b90-140">OUTPUTS</span></span>

### <span data-ttu-id="b6b90-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b6b90-141">System.Boolean</span></span>

## <span data-ttu-id="b6b90-142">筆記</span><span class="sxs-lookup"><span data-stu-id="b6b90-142">NOTES</span></span>

## <span data-ttu-id="b6b90-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6b90-143">RELATED LINKS</span></span>
