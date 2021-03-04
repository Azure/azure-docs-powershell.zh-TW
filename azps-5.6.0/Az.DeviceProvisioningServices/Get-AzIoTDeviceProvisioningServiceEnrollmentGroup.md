---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 037e2d99b52e6be1aeca3e74f2a31f3c0323749d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917757"
---
# <span data-ttu-id="96315-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="96315-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="96315-102">簡介</span><span class="sxs-lookup"><span data-stu-id="96315-102">SYNOPSIS</span></span>
<span data-ttu-id="96315-103">取得裝置註冊群組。</span><span class="sxs-lookup"><span data-stu-id="96315-103">Get a device enrollment group.</span></span>

## <span data-ttu-id="96315-104">語法</span><span class="sxs-lookup"><span data-stu-id="96315-104">SYNTAX</span></span>

### <span data-ttu-id="96315-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="96315-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96315-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="96315-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96315-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="96315-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96315-108">描述</span><span class="sxs-lookup"><span data-stu-id="96315-108">DESCRIPTION</span></span>
<span data-ttu-id="96315-109">取得 Azure IoT Hub 裝置設置服務中註冊群組或列出所有註冊群組的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="96315-109">Get the details of an enrollment group or list all enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="96315-110">例子</span><span class="sxs-lookup"><span data-stu-id="96315-110">EXAMPLES</span></span>

### <span data-ttu-id="96315-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="96315-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1"
```

<span data-ttu-id="96315-112">在 Azure IoT Hub 裝置設置服務中取得裝置註冊群組。</span><span class="sxs-lookup"><span data-stu-id="96315-112">Get device enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="96315-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="96315-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="96315-114">列出 Azure IoT Hub 裝置設置服務中所有裝置註冊群組。</span><span class="sxs-lookup"><span data-stu-id="96315-114">List all device enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="96315-115">參數</span><span class="sxs-lookup"><span data-stu-id="96315-115">PARAMETERS</span></span>

### <span data-ttu-id="96315-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96315-116">-DefaultProfile</span></span>
<span data-ttu-id="96315-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="96315-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96315-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="96315-118">-DpsName</span></span>
<span data-ttu-id="96315-119">IoT 裝置設置服務的名稱</span><span class="sxs-lookup"><span data-stu-id="96315-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="96315-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="96315-120">-DpsObject</span></span>
<span data-ttu-id="96315-121">IoT 裝置設置服務物件</span><span class="sxs-lookup"><span data-stu-id="96315-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="96315-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="96315-122">-Name</span></span>
<span data-ttu-id="96315-123">註冊組的名稱。</span><span class="sxs-lookup"><span data-stu-id="96315-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="96315-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96315-124">-ResourceGroupName</span></span>
<span data-ttu-id="96315-125">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="96315-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="96315-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96315-126">-ResourceId</span></span>
<span data-ttu-id="96315-127">IoT 裝置資源識別碼</span><span class="sxs-lookup"><span data-stu-id="96315-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="96315-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96315-128">CommonParameters</span></span>
<span data-ttu-id="96315-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="96315-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96315-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="96315-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96315-131">輸入</span><span class="sxs-lookup"><span data-stu-id="96315-131">INPUTS</span></span>

### <span data-ttu-id="96315-132">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="96315-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="96315-133">System.String</span><span class="sxs-lookup"><span data-stu-id="96315-133">System.String</span></span>

## <span data-ttu-id="96315-134">輸出</span><span class="sxs-lookup"><span data-stu-id="96315-134">OUTPUTS</span></span>

### <span data-ttu-id="96315-135">Microsoft.Azure.Commands.management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="96315-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

### <span data-ttu-id="96315-136">Microsoft.Azure.Commands.management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span><span class="sxs-lookup"><span data-stu-id="96315-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span></span>

## <span data-ttu-id="96315-137">筆記</span><span class="sxs-lookup"><span data-stu-id="96315-137">NOTES</span></span>

## <span data-ttu-id="96315-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="96315-138">RELATED LINKS</span></span>
