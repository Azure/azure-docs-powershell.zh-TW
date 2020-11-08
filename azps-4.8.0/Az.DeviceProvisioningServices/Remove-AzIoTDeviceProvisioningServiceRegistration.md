---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: b0fa84887a54eb1f4e9c689c49fb08a1300cd62b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129552"
---
# <span data-ttu-id="fd479-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="fd479-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="fd479-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fd479-102">SYNOPSIS</span></span>
<span data-ttu-id="fd479-103">刪除裝置註冊。</span><span class="sxs-lookup"><span data-stu-id="fd479-103">Deletes the device registration.</span></span>

## <span data-ttu-id="fd479-104">句法</span><span class="sxs-lookup"><span data-stu-id="fd479-104">SYNTAX</span></span>

### <span data-ttu-id="fd479-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fd479-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd479-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fd479-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd479-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fd479-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> -RegistrationId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd479-108">說明</span><span class="sxs-lookup"><span data-stu-id="fd479-108">DESCRIPTION</span></span>
<span data-ttu-id="fd479-109">刪除 Azure IoT 中心裝置的 [提供服務] 中的裝置註冊。</span><span class="sxs-lookup"><span data-stu-id="fd479-109">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="fd479-110">示例</span><span class="sxs-lookup"><span data-stu-id="fd479-110">EXAMPLES</span></span>

### <span data-ttu-id="fd479-111">範例1</span><span class="sxs-lookup"><span data-stu-id="fd479-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="fd479-112">刪除 Azure IoT 中心裝置的 [提供服務] 中的裝置註冊。</span><span class="sxs-lookup"><span data-stu-id="fd479-112">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="fd479-113">參數</span><span class="sxs-lookup"><span data-stu-id="fd479-113">PARAMETERS</span></span>

### <span data-ttu-id="fd479-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd479-114">-DefaultProfile</span></span>
<span data-ttu-id="fd479-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fd479-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd479-116">-DpsName</span><span class="sxs-lookup"><span data-stu-id="fd479-116">-DpsName</span></span>
<span data-ttu-id="fd479-117">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="fd479-117">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="fd479-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="fd479-118">-DpsObject</span></span>
<span data-ttu-id="fd479-119">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="fd479-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="fd479-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd479-120">-PassThru</span></span>
<span data-ttu-id="fd479-121">允許傳回布林值物件。</span><span class="sxs-lookup"><span data-stu-id="fd479-121">Allows to return the boolean object.</span></span>
<span data-ttu-id="fd479-122">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="fd479-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fd479-123">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="fd479-123">-RegistrationId</span></span>
<span data-ttu-id="fd479-124">裝置註冊的 ID。</span><span class="sxs-lookup"><span data-stu-id="fd479-124">ID of device registration.</span></span>

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

### <span data-ttu-id="fd479-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd479-125">-ResourceGroupName</span></span>
<span data-ttu-id="fd479-126">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="fd479-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fd479-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd479-127">-ResourceId</span></span>
<span data-ttu-id="fd479-128">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="fd479-128">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="fd479-129">-確認</span><span class="sxs-lookup"><span data-stu-id="fd479-129">-Confirm</span></span>
<span data-ttu-id="fd479-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fd479-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd479-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd479-131">-WhatIf</span></span>
<span data-ttu-id="fd479-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fd479-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd479-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fd479-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd479-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd479-134">CommonParameters</span></span>
<span data-ttu-id="fd479-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fd479-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd479-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fd479-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd479-137">輸入</span><span class="sxs-lookup"><span data-stu-id="fd479-137">INPUTS</span></span>

### <span data-ttu-id="fd479-138">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="fd479-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="fd479-139">System.object</span><span class="sxs-lookup"><span data-stu-id="fd479-139">System.String</span></span>

## <span data-ttu-id="fd479-140">輸出</span><span class="sxs-lookup"><span data-stu-id="fd479-140">OUTPUTS</span></span>

### <span data-ttu-id="fd479-141">System.object</span><span class="sxs-lookup"><span data-stu-id="fd479-141">System.Boolean</span></span>

## <span data-ttu-id="fd479-142">筆記</span><span class="sxs-lookup"><span data-stu-id="fd479-142">NOTES</span></span>

## <span data-ttu-id="fd479-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd479-143">RELATED LINKS</span></span>