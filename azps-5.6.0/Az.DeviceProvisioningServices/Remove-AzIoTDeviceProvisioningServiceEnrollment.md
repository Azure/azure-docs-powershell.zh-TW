---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: edf3845d9c4ac8a836212895fce2e5bbf4e40570
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910242"
---
# <span data-ttu-id="c1161-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="c1161-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="c1161-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c1161-102">SYNOPSIS</span></span>
<span data-ttu-id="c1161-103">刪除裝置註冊記錄。</span><span class="sxs-lookup"><span data-stu-id="c1161-103">Delete a device enrollment record.</span></span>

## <span data-ttu-id="c1161-104">語法</span><span class="sxs-lookup"><span data-stu-id="c1161-104">SYNTAX</span></span>

### <span data-ttu-id="c1161-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c1161-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1161-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c1161-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1161-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c1161-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1161-108">描述</span><span class="sxs-lookup"><span data-stu-id="c1161-108">DESCRIPTION</span></span>
<span data-ttu-id="c1161-109">刪除 Azure IoT Hub 裝置設置服務中的裝置註冊。</span><span class="sxs-lookup"><span data-stu-id="c1161-109">Delete a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="c1161-110">例子</span><span class="sxs-lookup"><span data-stu-id="c1161-110">EXAMPLES</span></span>

### <span data-ttu-id="c1161-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="c1161-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="c1161-112">刪除指定的註冊記錄。</span><span class="sxs-lookup"><span data-stu-id="c1161-112">Delete a specified enrollment record.</span></span>

### <span data-ttu-id="c1161-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="c1161-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="c1161-114">刪除所有註冊記錄。</span><span class="sxs-lookup"><span data-stu-id="c1161-114">Delete all enrollment records.</span></span>

## <span data-ttu-id="c1161-115">參數</span><span class="sxs-lookup"><span data-stu-id="c1161-115">PARAMETERS</span></span>

### <span data-ttu-id="c1161-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1161-116">-DefaultProfile</span></span>
<span data-ttu-id="c1161-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1161-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1161-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="c1161-118">-DpsName</span></span>
<span data-ttu-id="c1161-119">IoT 裝置設置服務的名稱</span><span class="sxs-lookup"><span data-stu-id="c1161-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c1161-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="c1161-120">-DpsObject</span></span>
<span data-ttu-id="c1161-121">IoT 裝置設置服務物件</span><span class="sxs-lookup"><span data-stu-id="c1161-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="c1161-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1161-122">-PassThru</span></span>
<span data-ttu-id="c1161-123">允許返回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="c1161-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="c1161-124">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="c1161-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c1161-125">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="c1161-125">-RegistrationId</span></span>
<span data-ttu-id="c1161-126">個別註冊註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="c1161-126">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="c1161-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1161-127">-ResourceGroupName</span></span>
<span data-ttu-id="c1161-128">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="c1161-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c1161-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1161-129">-ResourceId</span></span>
<span data-ttu-id="c1161-130">IoT 裝置資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c1161-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="c1161-131">-確認</span><span class="sxs-lookup"><span data-stu-id="c1161-131">-Confirm</span></span>
<span data-ttu-id="c1161-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c1161-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1161-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1161-133">-WhatIf</span></span>
<span data-ttu-id="c1161-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c1161-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1161-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1161-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1161-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1161-136">CommonParameters</span></span>
<span data-ttu-id="c1161-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c1161-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1161-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="c1161-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1161-139">輸入</span><span class="sxs-lookup"><span data-stu-id="c1161-139">INPUTS</span></span>

### <span data-ttu-id="c1161-140">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="c1161-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="c1161-141">System.String</span><span class="sxs-lookup"><span data-stu-id="c1161-141">System.String</span></span>

## <span data-ttu-id="c1161-142">輸出</span><span class="sxs-lookup"><span data-stu-id="c1161-142">OUTPUTS</span></span>

### <span data-ttu-id="c1161-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c1161-143">System.Boolean</span></span>

## <span data-ttu-id="c1161-144">筆記</span><span class="sxs-lookup"><span data-stu-id="c1161-144">NOTES</span></span>

## <span data-ttu-id="c1161-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1161-145">RELATED LINKS</span></span>
