---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: f4cac1380a6ed089d3b3e7b368eb15486e4c12d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135997"
---
# <span data-ttu-id="1f8fd-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="1f8fd-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="1f8fd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f8fd-102">SYNOPSIS</span></span>
<span data-ttu-id="1f8fd-103">取得裝置註冊群組。</span><span class="sxs-lookup"><span data-stu-id="1f8fd-103">Get a device enrollment group.</span></span>

## <span data-ttu-id="1f8fd-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f8fd-104">SYNTAX</span></span>

### <span data-ttu-id="1f8fd-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1f8fd-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f8fd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1f8fd-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f8fd-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1f8fd-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f8fd-108">說明</span><span class="sxs-lookup"><span data-stu-id="1f8fd-108">DESCRIPTION</span></span>
<span data-ttu-id="1f8fd-109">取得 Azure IoT 中心裝置預配服務中的註冊群組或清單的所有註冊群組的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1f8fd-109">Get the details of an enrollment group or list all enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="1f8fd-110">示例</span><span class="sxs-lookup"><span data-stu-id="1f8fd-110">EXAMPLES</span></span>

### <span data-ttu-id="1f8fd-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1f8fd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1"
```

<span data-ttu-id="1f8fd-112">在 Azure IoT 中樞裝置提供服務中取得裝置註冊群組。</span><span class="sxs-lookup"><span data-stu-id="1f8fd-112">Get device enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="1f8fd-113">範例2</span><span class="sxs-lookup"><span data-stu-id="1f8fd-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="1f8fd-114">列出 Azure IoT 中心裝置提供服務中的所有裝置註冊群組。</span><span class="sxs-lookup"><span data-stu-id="1f8fd-114">List all device enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="1f8fd-115">參數</span><span class="sxs-lookup"><span data-stu-id="1f8fd-115">PARAMETERS</span></span>

### <span data-ttu-id="1f8fd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f8fd-116">-DefaultProfile</span></span>
<span data-ttu-id="1f8fd-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f8fd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f8fd-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="1f8fd-118">-DpsName</span></span>
<span data-ttu-id="1f8fd-119">IoT 裝置預配服務的名稱</span><span class="sxs-lookup"><span data-stu-id="1f8fd-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="1f8fd-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="1f8fd-120">-DpsObject</span></span>
<span data-ttu-id="1f8fd-121">IoT 裝置置備服務物件</span><span class="sxs-lookup"><span data-stu-id="1f8fd-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="1f8fd-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f8fd-122">-Name</span></span>
<span data-ttu-id="1f8fd-123">註冊群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1f8fd-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="1f8fd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f8fd-124">-ResourceGroupName</span></span>
<span data-ttu-id="1f8fd-125">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="1f8fd-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1f8fd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f8fd-126">-ResourceId</span></span>
<span data-ttu-id="1f8fd-127">IoT 裝置預配服務資源識別碼</span><span class="sxs-lookup"><span data-stu-id="1f8fd-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="1f8fd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f8fd-128">CommonParameters</span></span>
<span data-ttu-id="1f8fd-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f8fd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f8fd-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1f8fd-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f8fd-131">輸入</span><span class="sxs-lookup"><span data-stu-id="1f8fd-131">INPUTS</span></span>

### <span data-ttu-id="1f8fd-132">PSProvisioningServiceDescription （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="1f8fd-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="1f8fd-133">System.object</span><span class="sxs-lookup"><span data-stu-id="1f8fd-133">System.String</span></span>

## <span data-ttu-id="1f8fd-134">輸出</span><span class="sxs-lookup"><span data-stu-id="1f8fd-134">OUTPUTS</span></span>

### <span data-ttu-id="1f8fd-135">PSEnrollmentGroup （DeviceProvisioningServices.）。</span><span class="sxs-lookup"><span data-stu-id="1f8fd-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

### <span data-ttu-id="1f8fd-136">PSEnrollmentGroups []. DeviceProvisioningServices. []</span><span class="sxs-lookup"><span data-stu-id="1f8fd-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span></span>

## <span data-ttu-id="1f8fd-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1f8fd-137">NOTES</span></span>

## <span data-ttu-id="1f8fd-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f8fd-138">RELATED LINKS</span></span>
