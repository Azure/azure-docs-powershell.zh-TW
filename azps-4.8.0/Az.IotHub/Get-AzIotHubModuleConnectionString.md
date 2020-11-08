---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduleconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
ms.openlocfilehash: 30926eaad6447f109b1755d419be0b3931a76054
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136366"
---
# <span data-ttu-id="72816-101">Get-AzIotHubModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="72816-101">Get-AzIotHubModuleConnectionString</span></span>

## <span data-ttu-id="72816-102">摘要</span><span class="sxs-lookup"><span data-stu-id="72816-102">SYNOPSIS</span></span>
<span data-ttu-id="72816-103">在 Iot 中樞中取得目標 IoT 裝置模組的連線字串。</span><span class="sxs-lookup"><span data-stu-id="72816-103">Get the connection string of a target IoT device module in an Iot Hub.</span></span>

## <span data-ttu-id="72816-104">句法</span><span class="sxs-lookup"><span data-stu-id="72816-104">SYNTAX</span></span>

### <span data-ttu-id="72816-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="72816-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72816-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="72816-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleConnectionString [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72816-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="72816-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72816-108">說明</span><span class="sxs-lookup"><span data-stu-id="72816-108">DESCRIPTION</span></span>
<span data-ttu-id="72816-109">列出 Azure IoT 中樞內包含之目標 IoT 裝置的所有模組或指定模組的連線字串。</span><span class="sxs-lookup"><span data-stu-id="72816-109">List connection string of all modules or a specified module of a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="72816-110">示例</span><span class="sxs-lookup"><span data-stu-id="72816-110">EXAMPLES</span></span>

### <span data-ttu-id="72816-111">範例1</span><span class="sxs-lookup"><span data-stu-id="72816-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Deviceid "myDevice1"

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******     
module2   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module2;x509=true
```

<span data-ttu-id="72816-112">在 Iot 中樞中顯示目標 IoT 裝置的所有模組連線字串。</span><span class="sxs-lookup"><span data-stu-id="72816-112">Show all modules connection string of a target IoT device in an Iot Hub.</span></span>

### <span data-ttu-id="72816-113">範例2</span><span class="sxs-lookup"><span data-stu-id="72816-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubMCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "module1" -KeyType secondary

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******
```

<span data-ttu-id="72816-114">在 Iot 中樞中取得目標 IoT 裝置的第二個模組連線字串。</span><span class="sxs-lookup"><span data-stu-id="72816-114">Get the secondary module connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="72816-115">參數</span><span class="sxs-lookup"><span data-stu-id="72816-115">PARAMETERS</span></span>

### <span data-ttu-id="72816-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72816-116">-DefaultProfile</span></span>
<span data-ttu-id="72816-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="72816-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72816-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="72816-118">-DeviceId</span></span>
<span data-ttu-id="72816-119">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="72816-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72816-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72816-120">-InputObject</span></span>
<span data-ttu-id="72816-121">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="72816-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72816-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="72816-122">-IotHubName</span></span>
<span data-ttu-id="72816-123">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="72816-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="72816-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="72816-124">-KeyType</span></span>
<span data-ttu-id="72816-125">Auth 的共用存取原則金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="72816-125">Shared access policy key type for auth.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72816-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="72816-126">-ModuleId</span></span>
<span data-ttu-id="72816-127">目的模組識別碼。</span><span class="sxs-lookup"><span data-stu-id="72816-127">Target Module Id.</span></span>

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

### <span data-ttu-id="72816-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72816-128">-ResourceGroupName</span></span>
<span data-ttu-id="72816-129">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="72816-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="72816-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72816-130">-ResourceId</span></span>
<span data-ttu-id="72816-131">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="72816-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="72816-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72816-132">CommonParameters</span></span>
<span data-ttu-id="72816-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="72816-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72816-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="72816-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72816-135">輸入</span><span class="sxs-lookup"><span data-stu-id="72816-135">INPUTS</span></span>

### <span data-ttu-id="72816-136">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="72816-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="72816-137">System.object</span><span class="sxs-lookup"><span data-stu-id="72816-137">System.String</span></span>

## <span data-ttu-id="72816-138">輸出</span><span class="sxs-lookup"><span data-stu-id="72816-138">OUTPUTS</span></span>

### <span data-ttu-id="72816-139">PSModuleConnectionString （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="72816-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span></span>

## <span data-ttu-id="72816-140">筆記</span><span class="sxs-lookup"><span data-stu-id="72816-140">NOTES</span></span>

## <span data-ttu-id="72816-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="72816-141">RELATED LINKS</span></span>
