---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: dfca2885c644f35ba26a0cf9e15bff16c6156528
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436561"
---
# <span data-ttu-id="6ab0b-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="6ab0b-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="6ab0b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ab0b-102">SYNOPSIS</span></span>
<span data-ttu-id="6ab0b-103">取得裝置註冊記錄。</span><span class="sxs-lookup"><span data-stu-id="6ab0b-103">Get a device enrollment record.</span></span>

## <span data-ttu-id="6ab0b-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ab0b-104">SYNTAX</span></span>

### <span data-ttu-id="6ab0b-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6ab0b-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ab0b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6ab0b-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ab0b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6ab0b-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ab0b-108">說明</span><span class="sxs-lookup"><span data-stu-id="6ab0b-108">DESCRIPTION</span></span>
<span data-ttu-id="6ab0b-109">在 Azure IoT 中樞裝置的 [提供服務] 中取得裝置註冊詳細資料或清單設備註冊。</span><span class="sxs-lookup"><span data-stu-id="6ab0b-109">Get device enrollment details or List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="6ab0b-110">示例</span><span class="sxs-lookup"><span data-stu-id="6ab0b-110">EXAMPLES</span></span>

### <span data-ttu-id="6ab0b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="6ab0b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="6ab0b-112">在 Azure IoT 中樞裝置提供服務中取得裝置註冊的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6ab0b-112">Get device enrollment details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="6ab0b-113">範例2</span><span class="sxs-lookup"><span data-stu-id="6ab0b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="6ab0b-114">在 Azure IoT 中樞裝置的 [提供服務] 中，列出裝置註冊。</span><span class="sxs-lookup"><span data-stu-id="6ab0b-114">List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="6ab0b-115">參數</span><span class="sxs-lookup"><span data-stu-id="6ab0b-115">PARAMETERS</span></span>

### <span data-ttu-id="6ab0b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab0b-116">-DefaultProfile</span></span>
<span data-ttu-id="6ab0b-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ab0b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ab0b-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="6ab0b-118">-DpsName</span></span>
<span data-ttu-id="6ab0b-119">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="6ab0b-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="6ab0b-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="6ab0b-120">-DpsObject</span></span>
<span data-ttu-id="6ab0b-121">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="6ab0b-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="6ab0b-122">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="6ab0b-122">-RegistrationId</span></span>
<span data-ttu-id="6ab0b-123">個人登記登記 id。</span><span class="sxs-lookup"><span data-stu-id="6ab0b-123">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="6ab0b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ab0b-124">-ResourceGroupName</span></span>
<span data-ttu-id="6ab0b-125">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="6ab0b-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6ab0b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ab0b-126">-ResourceId</span></span>
<span data-ttu-id="6ab0b-127">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6ab0b-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="6ab0b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab0b-128">CommonParameters</span></span>
<span data-ttu-id="6ab0b-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ab0b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab0b-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6ab0b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab0b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="6ab0b-131">INPUTS</span></span>

### <span data-ttu-id="6ab0b-132">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="6ab0b-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="6ab0b-133">System.object</span><span class="sxs-lookup"><span data-stu-id="6ab0b-133">System.String</span></span>

## <span data-ttu-id="6ab0b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="6ab0b-134">OUTPUTS</span></span>

### <span data-ttu-id="6ab0b-135">PSIndividualEnrollment （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="6ab0b-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

### <span data-ttu-id="6ab0b-136">PSIndividualEnrollments []. DeviceProvisioningServices. []</span><span class="sxs-lookup"><span data-stu-id="6ab0b-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span></span>

## <span data-ttu-id="6ab0b-137">筆記</span><span class="sxs-lookup"><span data-stu-id="6ab0b-137">NOTES</span></span>

## <span data-ttu-id="6ab0b-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ab0b-138">RELATED LINKS</span></span>
