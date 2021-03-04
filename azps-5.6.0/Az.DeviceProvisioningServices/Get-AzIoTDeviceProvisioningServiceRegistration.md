---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: 6d3997e8a58ecab6a31e233d4ee3c0e2c66ae9ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912865"
---
# <span data-ttu-id="8854e-101">Get-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="8854e-101">Get-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="8854e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8854e-102">SYNOPSIS</span></span>
<span data-ttu-id="8854e-103">獲得裝置註冊狀態。</span><span class="sxs-lookup"><span data-stu-id="8854e-103">Gets the device registration state.</span></span>

## <span data-ttu-id="8854e-104">語法</span><span class="sxs-lookup"><span data-stu-id="8854e-104">SYNTAX</span></span>

### <span data-ttu-id="8854e-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8854e-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8854e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8854e-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8854e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8854e-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> [-RegistrationId <String>]
 [-EnrollmentId <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8854e-108">描述</span><span class="sxs-lookup"><span data-stu-id="8854e-108">DESCRIPTION</span></span>
<span data-ttu-id="8854e-109">在 Azure IoT 中心裝置設置服務中的註冊組下取得裝置註冊狀態或裝置註冊狀態。</span><span class="sxs-lookup"><span data-stu-id="8854e-109">Get the device registration state or the registration state of devices under the enrollmentGroup in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="8854e-110">例子</span><span class="sxs-lookup"><span data-stu-id="8854e-110">EXAMPLES</span></span>

### <span data-ttu-id="8854e-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="8854e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="8854e-112">在 Azure IoT Hub 裝置設置服務中取得裝置註冊狀態詳細資料。</span><span class="sxs-lookup"><span data-stu-id="8854e-112">Get the device registration state details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="8854e-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="8854e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -EnrollmentId "grp-enroll1"
```

<span data-ttu-id="8854e-114">列出此註冊Group 中裝置的所有註冊狀態。</span><span class="sxs-lookup"><span data-stu-id="8854e-114">List all the registration state of devices in this enrollmentGroup.</span></span>

## <span data-ttu-id="8854e-115">參數</span><span class="sxs-lookup"><span data-stu-id="8854e-115">PARAMETERS</span></span>

### <span data-ttu-id="8854e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8854e-116">-DefaultProfile</span></span>
<span data-ttu-id="8854e-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8854e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8854e-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="8854e-118">-DpsName</span></span>
<span data-ttu-id="8854e-119">IoT 裝置設置服務的名稱</span><span class="sxs-lookup"><span data-stu-id="8854e-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="8854e-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="8854e-120">-DpsObject</span></span>
<span data-ttu-id="8854e-121">IoT 裝置設置服務物件</span><span class="sxs-lookup"><span data-stu-id="8854e-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="8854e-122">-EnrollmentId</span><span class="sxs-lookup"><span data-stu-id="8854e-122">-EnrollmentId</span></span>
<span data-ttu-id="8854e-123">註冊群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8854e-123">ID of enrollment group.</span></span>

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

### <span data-ttu-id="8854e-124">-查詢</span><span class="sxs-lookup"><span data-stu-id="8854e-124">-Query</span></span>
<span data-ttu-id="8854e-125">Sql 查詢。</span><span class="sxs-lookup"><span data-stu-id="8854e-125">Sql query.</span></span>

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

### <span data-ttu-id="8854e-126">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="8854e-126">-RegistrationId</span></span>
<span data-ttu-id="8854e-127">裝置註冊的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8854e-127">ID of device registration.</span></span>

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

### <span data-ttu-id="8854e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8854e-128">-ResourceGroupName</span></span>
<span data-ttu-id="8854e-129">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="8854e-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8854e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8854e-130">-ResourceId</span></span>
<span data-ttu-id="8854e-131">IoT 裝置資源識別碼</span><span class="sxs-lookup"><span data-stu-id="8854e-131">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="8854e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8854e-132">CommonParameters</span></span>
<span data-ttu-id="8854e-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8854e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8854e-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8854e-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8854e-135">輸入</span><span class="sxs-lookup"><span data-stu-id="8854e-135">INPUTS</span></span>

### <span data-ttu-id="8854e-136">Microsoft.Azure.Commands.management.DeviceProvisioningServices.models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="8854e-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="8854e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="8854e-137">System.String</span></span>

## <span data-ttu-id="8854e-138">輸出</span><span class="sxs-lookup"><span data-stu-id="8854e-138">OUTPUTS</span></span>

### <span data-ttu-id="8854e-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="8854e-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span></span>

### <span data-ttu-id="8854e-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span><span class="sxs-lookup"><span data-stu-id="8854e-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span></span>

## <span data-ttu-id="8854e-141">筆記</span><span class="sxs-lookup"><span data-stu-id="8854e-141">NOTES</span></span>

## <span data-ttu-id="8854e-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="8854e-142">RELATED LINKS</span></span>
