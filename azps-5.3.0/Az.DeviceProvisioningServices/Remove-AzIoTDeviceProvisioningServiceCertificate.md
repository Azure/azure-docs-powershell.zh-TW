---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 566594fef5741808e4f27ccb6d1996783b5c880b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435190"
---
# <span data-ttu-id="fc5aa-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="fc5aa-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="fc5aa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc5aa-102">SYNOPSIS</span></span>
<span data-ttu-id="fc5aa-103">刪除 Azure IoT 中樞裝置預配服務憑證。</span><span class="sxs-lookup"><span data-stu-id="fc5aa-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="fc5aa-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc5aa-104">SYNTAX</span></span>

### <span data-ttu-id="fc5aa-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fc5aa-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc5aa-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fc5aa-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc5aa-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fc5aa-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc5aa-108">說明</span><span class="sxs-lookup"><span data-stu-id="fc5aa-108">DESCRIPTION</span></span>
<span data-ttu-id="fc5aa-109">如需 Azure IoT 中樞裝置提供服務中 CA 憑證的詳細說明，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates 。</span><span class="sxs-lookup"><span data-stu-id="fc5aa-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="fc5aa-110">示例</span><span class="sxs-lookup"><span data-stu-id="fc5aa-110">EXAMPLES</span></span>

### <span data-ttu-id="fc5aa-111">範例1</span><span class="sxs-lookup"><span data-stu-id="fc5aa-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="fc5aa-112">在 Azure IoT 中樞裝置的 [提供服務] 中刪除 "mycertificate"。</span><span class="sxs-lookup"><span data-stu-id="fc5aa-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="fc5aa-113">參數</span><span class="sxs-lookup"><span data-stu-id="fc5aa-113">PARAMETERS</span></span>

### <span data-ttu-id="fc5aa-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="fc5aa-114">-CertificateName</span></span>
<span data-ttu-id="fc5aa-115">憑證的名稱</span><span class="sxs-lookup"><span data-stu-id="fc5aa-115">Name of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc5aa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc5aa-116">-DefaultProfile</span></span>
<span data-ttu-id="fc5aa-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fc5aa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc5aa-118">-Etag</span><span class="sxs-lookup"><span data-stu-id="fc5aa-118">-Etag</span></span>
<span data-ttu-id="fc5aa-119">憑證的 Etag</span><span class="sxs-lookup"><span data-stu-id="fc5aa-119">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc5aa-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc5aa-120">-InputObject</span></span>
<span data-ttu-id="fc5aa-121">IoT 裝置預配服務憑證物件</span><span class="sxs-lookup"><span data-stu-id="fc5aa-121">IoT Device Provisioning Service Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc5aa-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="fc5aa-122">-Name</span></span>
<span data-ttu-id="fc5aa-123">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="fc5aa-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="fc5aa-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc5aa-124">-PassThru</span></span>
<span data-ttu-id="fc5aa-125">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="fc5aa-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fc5aa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc5aa-126">-ResourceGroupName</span></span>
<span data-ttu-id="fc5aa-127">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="fc5aa-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fc5aa-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc5aa-128">-ResourceId</span></span>
<span data-ttu-id="fc5aa-129">IoT 裝置預配服務憑證資源識別碼</span><span class="sxs-lookup"><span data-stu-id="fc5aa-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="fc5aa-130">-確認</span><span class="sxs-lookup"><span data-stu-id="fc5aa-130">-Confirm</span></span>
<span data-ttu-id="fc5aa-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fc5aa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc5aa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc5aa-132">-WhatIf</span></span>
<span data-ttu-id="fc5aa-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fc5aa-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc5aa-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fc5aa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc5aa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc5aa-135">CommonParameters</span></span>
<span data-ttu-id="fc5aa-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc5aa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc5aa-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fc5aa-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc5aa-138">輸入</span><span class="sxs-lookup"><span data-stu-id="fc5aa-138">INPUTS</span></span>

### <span data-ttu-id="fc5aa-139">PSCertificateResponse （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="fc5aa-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="fc5aa-140">System.object</span><span class="sxs-lookup"><span data-stu-id="fc5aa-140">System.String</span></span>

## <span data-ttu-id="fc5aa-141">輸出</span><span class="sxs-lookup"><span data-stu-id="fc5aa-141">OUTPUTS</span></span>

### <span data-ttu-id="fc5aa-142">System.object</span><span class="sxs-lookup"><span data-stu-id="fc5aa-142">System.Boolean</span></span>

## <span data-ttu-id="fc5aa-143">筆記</span><span class="sxs-lookup"><span data-stu-id="fc5aa-143">NOTES</span></span>

## <span data-ttu-id="fc5aa-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc5aa-144">RELATED LINKS</span></span>
