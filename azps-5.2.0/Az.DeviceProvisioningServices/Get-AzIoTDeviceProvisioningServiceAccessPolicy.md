---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 87c6bdd72229baec8e65c40d4e2e4309bde59aba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274863"
---
# <span data-ttu-id="89c46-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="89c46-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="89c46-102">摘要</span><span class="sxs-lookup"><span data-stu-id="89c46-102">SYNOPSIS</span></span>
<span data-ttu-id="89c46-103">在 Azure IoT 中樞裝置置備服務中，列出全部或顯示共用訪問原則的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="89c46-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="89c46-104">句法</span><span class="sxs-lookup"><span data-stu-id="89c46-104">SYNTAX</span></span>

### <span data-ttu-id="89c46-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="89c46-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89c46-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="89c46-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89c46-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="89c46-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89c46-108">說明</span><span class="sxs-lookup"><span data-stu-id="89c46-108">DESCRIPTION</span></span>
<span data-ttu-id="89c46-109">如需 Azure IoT 中樞裝置置備服務的簡介，請參閱 https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps 。</span><span class="sxs-lookup"><span data-stu-id="89c46-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="89c46-110">示例</span><span class="sxs-lookup"><span data-stu-id="89c46-110">EXAMPLES</span></span>

### <span data-ttu-id="89c46-111">範例1</span><span class="sxs-lookup"><span data-stu-id="89c46-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="89c46-112">在 "myiotdps" 中列出所有共用的存取原則。</span><span class="sxs-lookup"><span data-stu-id="89c46-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="89c46-113">範例2</span><span class="sxs-lookup"><span data-stu-id="89c46-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="89c46-114">顯示 Azure IoT 中樞裝置提供服務中共用存取原則 "mypolicy" 的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="89c46-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="89c46-115">參數</span><span class="sxs-lookup"><span data-stu-id="89c46-115">PARAMETERS</span></span>

### <span data-ttu-id="89c46-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89c46-116">-DefaultProfile</span></span>
<span data-ttu-id="89c46-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="89c46-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89c46-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="89c46-118">-DpsObject</span></span>
<span data-ttu-id="89c46-119">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="89c46-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="89c46-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="89c46-120">-KeyName</span></span>
<span data-ttu-id="89c46-121">IoT 裝置的提供服務存取原則金鑰名稱</span><span class="sxs-lookup"><span data-stu-id="89c46-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="89c46-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="89c46-122">-Name</span></span>
<span data-ttu-id="89c46-123">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="89c46-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="89c46-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89c46-124">-ResourceGroupName</span></span>
<span data-ttu-id="89c46-125">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="89c46-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="89c46-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89c46-126">-ResourceId</span></span>
<span data-ttu-id="89c46-127">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="89c46-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="89c46-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89c46-128">CommonParameters</span></span>
<span data-ttu-id="89c46-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="89c46-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89c46-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="89c46-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89c46-131">輸入</span><span class="sxs-lookup"><span data-stu-id="89c46-131">INPUTS</span></span>

### <span data-ttu-id="89c46-132">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="89c46-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="89c46-133">System.object</span><span class="sxs-lookup"><span data-stu-id="89c46-133">System.String</span></span>

## <span data-ttu-id="89c46-134">輸出</span><span class="sxs-lookup"><span data-stu-id="89c46-134">OUTPUTS</span></span>

### <span data-ttu-id="89c46-135">PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="89c46-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="89c46-136">筆記</span><span class="sxs-lookup"><span data-stu-id="89c46-136">NOTES</span></span>

## <span data-ttu-id="89c46-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="89c46-137">RELATED LINKS</span></span>
