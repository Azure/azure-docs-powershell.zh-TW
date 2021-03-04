---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 56aadda2d7f1dccb77795d5226fb79c8a0fc65ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903602"
---
# <span data-ttu-id="74b9e-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="74b9e-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="74b9e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="74b9e-102">SYNOPSIS</span></span>
<span data-ttu-id="74b9e-103">取得裝置註冊記錄。</span><span class="sxs-lookup"><span data-stu-id="74b9e-103">Get a device enrollment record.</span></span>

## <span data-ttu-id="74b9e-104">語法</span><span class="sxs-lookup"><span data-stu-id="74b9e-104">SYNTAX</span></span>

### <span data-ttu-id="74b9e-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="74b9e-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74b9e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="74b9e-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="74b9e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="74b9e-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74b9e-108">描述</span><span class="sxs-lookup"><span data-stu-id="74b9e-108">DESCRIPTION</span></span>
<span data-ttu-id="74b9e-109">取得 Azure IoT Hub 裝置設置服務中的裝置註冊詳細資料或清單裝置註冊。</span><span class="sxs-lookup"><span data-stu-id="74b9e-109">Get device enrollment details or List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="74b9e-110">例子</span><span class="sxs-lookup"><span data-stu-id="74b9e-110">EXAMPLES</span></span>

### <span data-ttu-id="74b9e-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="74b9e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="74b9e-112">在 Azure IoT Hub 裝置設置服務中取得裝置註冊詳細資料。</span><span class="sxs-lookup"><span data-stu-id="74b9e-112">Get device enrollment details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="74b9e-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="74b9e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="74b9e-114">在 Azure IoT 中心裝置設置服務中列出裝置註冊。</span><span class="sxs-lookup"><span data-stu-id="74b9e-114">List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="74b9e-115">參數</span><span class="sxs-lookup"><span data-stu-id="74b9e-115">PARAMETERS</span></span>

### <span data-ttu-id="74b9e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74b9e-116">-DefaultProfile</span></span>
<span data-ttu-id="74b9e-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="74b9e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74b9e-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="74b9e-118">-DpsName</span></span>
<span data-ttu-id="74b9e-119">IoT 裝置設置服務的名稱</span><span class="sxs-lookup"><span data-stu-id="74b9e-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="74b9e-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="74b9e-120">-DpsObject</span></span>
<span data-ttu-id="74b9e-121">IoT 裝置設置服務物件</span><span class="sxs-lookup"><span data-stu-id="74b9e-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="74b9e-122">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="74b9e-122">-RegistrationId</span></span>
<span data-ttu-id="74b9e-123">個別註冊註冊識別碼。</span><span class="sxs-lookup"><span data-stu-id="74b9e-123">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="74b9e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74b9e-124">-ResourceGroupName</span></span>
<span data-ttu-id="74b9e-125">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="74b9e-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="74b9e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74b9e-126">-ResourceId</span></span>
<span data-ttu-id="74b9e-127">IoT 裝置資源識別碼</span><span class="sxs-lookup"><span data-stu-id="74b9e-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="74b9e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74b9e-128">CommonParameters</span></span>
<span data-ttu-id="74b9e-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="74b9e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74b9e-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="74b9e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74b9e-131">輸入</span><span class="sxs-lookup"><span data-stu-id="74b9e-131">INPUTS</span></span>

### <span data-ttu-id="74b9e-132">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="74b9e-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="74b9e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="74b9e-133">System.String</span></span>

## <span data-ttu-id="74b9e-134">輸出</span><span class="sxs-lookup"><span data-stu-id="74b9e-134">OUTPUTS</span></span>

### <span data-ttu-id="74b9e-135">Microsoft.Azure.Commands.management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="74b9e-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

### <span data-ttu-id="74b9e-136">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSIndividualEnrollments[]</span><span class="sxs-lookup"><span data-stu-id="74b9e-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span></span>

## <span data-ttu-id="74b9e-137">筆記</span><span class="sxs-lookup"><span data-stu-id="74b9e-137">NOTES</span></span>

## <span data-ttu-id="74b9e-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="74b9e-138">RELATED LINKS</span></span>
