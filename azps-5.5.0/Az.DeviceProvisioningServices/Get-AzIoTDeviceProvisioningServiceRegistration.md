---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: 4951c75af3935d982d044ab02648915f980ff16e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132019"
---
# <span data-ttu-id="f0e54-101">Get-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="f0e54-101">Get-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="f0e54-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f0e54-102">SYNOPSIS</span></span>
<span data-ttu-id="f0e54-103">取得裝置註冊狀態。</span><span class="sxs-lookup"><span data-stu-id="f0e54-103">Gets the device registration state.</span></span>

## <span data-ttu-id="f0e54-104">句法</span><span class="sxs-lookup"><span data-stu-id="f0e54-104">SYNTAX</span></span>

### <span data-ttu-id="f0e54-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f0e54-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0e54-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f0e54-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0e54-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f0e54-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> [-RegistrationId <String>]
 [-EnrollmentId <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0e54-108">說明</span><span class="sxs-lookup"><span data-stu-id="f0e54-108">DESCRIPTION</span></span>
<span data-ttu-id="f0e54-109">在 Azure IoT 中樞裝置提供服務的 enrollmentGroup 下，取得裝置註冊狀態或裝置的註冊狀態。</span><span class="sxs-lookup"><span data-stu-id="f0e54-109">Get the device registration state or the registration state of devices under the enrollmentGroup in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="f0e54-110">示例</span><span class="sxs-lookup"><span data-stu-id="f0e54-110">EXAMPLES</span></span>

### <span data-ttu-id="f0e54-111">範例1</span><span class="sxs-lookup"><span data-stu-id="f0e54-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="f0e54-112">在 Azure IoT 中樞裝置預配服務中取得裝置註冊狀態的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f0e54-112">Get the device registration state details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="f0e54-113">範例2</span><span class="sxs-lookup"><span data-stu-id="f0e54-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -EnrollmentId "grp-enroll1"
```

<span data-ttu-id="f0e54-114">列出此 enrollmentGroup 中裝置的所有登錄狀態。</span><span class="sxs-lookup"><span data-stu-id="f0e54-114">List all the registration state of devices in this enrollmentGroup.</span></span>

## <span data-ttu-id="f0e54-115">參數</span><span class="sxs-lookup"><span data-stu-id="f0e54-115">PARAMETERS</span></span>

### <span data-ttu-id="f0e54-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0e54-116">-DefaultProfile</span></span>
<span data-ttu-id="f0e54-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f0e54-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0e54-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="f0e54-118">-DpsName</span></span>
<span data-ttu-id="f0e54-119">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="f0e54-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="f0e54-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="f0e54-120">-DpsObject</span></span>
<span data-ttu-id="f0e54-121">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="f0e54-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="f0e54-122">-EnrollmentId</span><span class="sxs-lookup"><span data-stu-id="f0e54-122">-EnrollmentId</span></span>
<span data-ttu-id="f0e54-123">註冊群組的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f0e54-123">ID of enrollment group.</span></span>

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

### <span data-ttu-id="f0e54-124">-Query</span><span class="sxs-lookup"><span data-stu-id="f0e54-124">-Query</span></span>
<span data-ttu-id="f0e54-125">Sql 查詢。</span><span class="sxs-lookup"><span data-stu-id="f0e54-125">Sql query.</span></span>

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

### <span data-ttu-id="f0e54-126">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="f0e54-126">-RegistrationId</span></span>
<span data-ttu-id="f0e54-127">裝置註冊的 ID。</span><span class="sxs-lookup"><span data-stu-id="f0e54-127">ID of device registration.</span></span>

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

### <span data-ttu-id="f0e54-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0e54-128">-ResourceGroupName</span></span>
<span data-ttu-id="f0e54-129">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="f0e54-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f0e54-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0e54-130">-ResourceId</span></span>
<span data-ttu-id="f0e54-131">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="f0e54-131">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="f0e54-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0e54-132">CommonParameters</span></span>
<span data-ttu-id="f0e54-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f0e54-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0e54-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f0e54-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0e54-135">輸入</span><span class="sxs-lookup"><span data-stu-id="f0e54-135">INPUTS</span></span>

### <span data-ttu-id="f0e54-136">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="f0e54-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="f0e54-137">System.object</span><span class="sxs-lookup"><span data-stu-id="f0e54-137">System.String</span></span>

## <span data-ttu-id="f0e54-138">輸出</span><span class="sxs-lookup"><span data-stu-id="f0e54-138">OUTPUTS</span></span>

### <span data-ttu-id="f0e54-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="f0e54-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span></span>

### <span data-ttu-id="f0e54-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates []</span><span class="sxs-lookup"><span data-stu-id="f0e54-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span></span>

## <span data-ttu-id="f0e54-141">筆記</span><span class="sxs-lookup"><span data-stu-id="f0e54-141">NOTES</span></span>

## <span data-ttu-id="f0e54-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="f0e54-142">RELATED LINKS</span></span>
