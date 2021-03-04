---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubmoduleconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
ms.openlocfilehash: 739153aebdaf8b089c0d180643056725a85f450a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911037"
---
# <span data-ttu-id="16751-101">Get-AzIotHubModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="16751-101">Get-AzIotHubModuleConnectionString</span></span>

## <span data-ttu-id="16751-102">簡介</span><span class="sxs-lookup"><span data-stu-id="16751-102">SYNOPSIS</span></span>
<span data-ttu-id="16751-103">取得 Iot Hub 中目標 IoT 裝置模組的連接字串。</span><span class="sxs-lookup"><span data-stu-id="16751-103">Get the connection string of a target IoT device module in an Iot Hub.</span></span>

## <span data-ttu-id="16751-104">語法</span><span class="sxs-lookup"><span data-stu-id="16751-104">SYNTAX</span></span>

### <span data-ttu-id="16751-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="16751-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16751-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="16751-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleConnectionString [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="16751-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="16751-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16751-108">描述</span><span class="sxs-lookup"><span data-stu-id="16751-108">DESCRIPTION</span></span>
<span data-ttu-id="16751-109">Azure IoT 中心內所包含之目標 IoT 裝置之所有模組或指定模組的清單連接字串。</span><span class="sxs-lookup"><span data-stu-id="16751-109">List connection string of all modules or a specified module of a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="16751-110">例子</span><span class="sxs-lookup"><span data-stu-id="16751-110">EXAMPLES</span></span>

### <span data-ttu-id="16751-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="16751-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Deviceid "myDevice1"

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******     
module2   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module2;x509=true
```

<span data-ttu-id="16751-112">在 Iot Hub 中顯示目標 IoT 裝置的所有模組連接字串。</span><span class="sxs-lookup"><span data-stu-id="16751-112">Show all modules connection string of a target IoT device in an Iot Hub.</span></span>

### <span data-ttu-id="16751-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="16751-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubMCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "module1" -KeyType secondary

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******
```

<span data-ttu-id="16751-114">取得 Iot Hub 中目標 IoT 裝置之次要模組連接字串。</span><span class="sxs-lookup"><span data-stu-id="16751-114">Get the secondary module connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="16751-115">參數</span><span class="sxs-lookup"><span data-stu-id="16751-115">PARAMETERS</span></span>

### <span data-ttu-id="16751-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16751-116">-DefaultProfile</span></span>
<span data-ttu-id="16751-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="16751-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16751-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="16751-118">-DeviceId</span></span>
<span data-ttu-id="16751-119">目標裝置識別碼。</span><span class="sxs-lookup"><span data-stu-id="16751-119">Target Device Id.</span></span>

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

### <span data-ttu-id="16751-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16751-120">-InputObject</span></span>
<span data-ttu-id="16751-121">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="16751-121">IotHub object</span></span>

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

### <span data-ttu-id="16751-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="16751-122">-IotHubName</span></span>
<span data-ttu-id="16751-123">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="16751-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="16751-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="16751-124">-KeyType</span></span>
<span data-ttu-id="16751-125">用於驗證的共用存取策略金鑰類型。</span><span class="sxs-lookup"><span data-stu-id="16751-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="16751-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="16751-126">-ModuleId</span></span>
<span data-ttu-id="16751-127">目的模組識別碼。</span><span class="sxs-lookup"><span data-stu-id="16751-127">Target Module Id.</span></span>

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

### <span data-ttu-id="16751-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16751-128">-ResourceGroupName</span></span>
<span data-ttu-id="16751-129">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="16751-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="16751-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16751-130">-ResourceId</span></span>
<span data-ttu-id="16751-131">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="16751-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="16751-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16751-132">CommonParameters</span></span>
<span data-ttu-id="16751-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="16751-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16751-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="16751-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16751-135">輸入</span><span class="sxs-lookup"><span data-stu-id="16751-135">INPUTS</span></span>

### <span data-ttu-id="16751-136">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="16751-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="16751-137">System.String</span><span class="sxs-lookup"><span data-stu-id="16751-137">System.String</span></span>

## <span data-ttu-id="16751-138">輸出</span><span class="sxs-lookup"><span data-stu-id="16751-138">OUTPUTS</span></span>

### <span data-ttu-id="16751-139">Microsoft.Azure.Commands.management.IotHub.models.PSModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="16751-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span></span>

## <span data-ttu-id="16751-140">筆記</span><span class="sxs-lookup"><span data-stu-id="16751-140">NOTES</span></span>

## <span data-ttu-id="16751-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="16751-141">RELATED LINKS</span></span>
