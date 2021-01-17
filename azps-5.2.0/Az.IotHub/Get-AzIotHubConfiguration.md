---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubConfiguration.md
ms.openlocfilehash: 616fface9f20609c043884754e9b3904ffc83e67
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275235"
---
# <span data-ttu-id="771c2-101">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="771c2-101">Get-AzIotHubConfiguration</span></span>

## <span data-ttu-id="771c2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="771c2-102">SYNOPSIS</span></span>
<span data-ttu-id="771c2-103">列出所有或特定的 IoT 自動裝置管理設定。</span><span class="sxs-lookup"><span data-stu-id="771c2-103">Lists all or a particular IoT automatic device management configuration.</span></span>

## <span data-ttu-id="771c2-104">句法</span><span class="sxs-lookup"><span data-stu-id="771c2-104">SYNTAX</span></span>

### <span data-ttu-id="771c2-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="771c2-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="771c2-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="771c2-106">InputObjectSet</span></span>
```
Get-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="771c2-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="771c2-107">ResourceIdSet</span></span>
```
Get-AzIotHubConfiguration [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="771c2-108">說明</span><span class="sxs-lookup"><span data-stu-id="771c2-108">DESCRIPTION</span></span>
<span data-ttu-id="771c2-109">取得 iot 中樞中 IoT 自動裝置管理設定或清單 IoT 自動裝置管理設定的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="771c2-109">Get the details of an IoT automatic device management configuration or list IoT automatic device management configurations in an IoT Hub.</span></span>
<span data-ttu-id="771c2-110">如需詳細資訊，請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management 。</span><span class="sxs-lookup"><span data-stu-id="771c2-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="771c2-111">示例</span><span class="sxs-lookup"><span data-stu-id="771c2-111">EXAMPLES</span></span>

### <span data-ttu-id="771c2-112">範例1</span><span class="sxs-lookup"><span data-stu-id="771c2-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="771c2-113">取得 IoT 自動裝置管理設定的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="771c2-113">Get the details of an IoT automatic device management configuration.</span></span>

### <span data-ttu-id="771c2-114">範例2</span><span class="sxs-lookup"><span data-stu-id="771c2-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="771c2-115">清單 IoT 中樞中的 IoT 自動裝置管理設定。</span><span class="sxs-lookup"><span data-stu-id="771c2-115">List IoT automatic device management configurations in an IoT Hub.</span></span>

## <span data-ttu-id="771c2-116">參數</span><span class="sxs-lookup"><span data-stu-id="771c2-116">PARAMETERS</span></span>

### <span data-ttu-id="771c2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="771c2-117">-DefaultProfile</span></span>
<span data-ttu-id="771c2-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="771c2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="771c2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="771c2-119">-InputObject</span></span>
<span data-ttu-id="771c2-120">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="771c2-120">IotHub object</span></span>

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

### <span data-ttu-id="771c2-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="771c2-121">-IotHubName</span></span>
<span data-ttu-id="771c2-122">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="771c2-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="771c2-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="771c2-123">-Name</span></span>
<span data-ttu-id="771c2-124">配置的識別碼。</span><span class="sxs-lookup"><span data-stu-id="771c2-124">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="771c2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="771c2-125">-ResourceGroupName</span></span>
<span data-ttu-id="771c2-126">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="771c2-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="771c2-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="771c2-127">-ResourceId</span></span>
<span data-ttu-id="771c2-128">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="771c2-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="771c2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="771c2-129">CommonParameters</span></span>
<span data-ttu-id="771c2-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="771c2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="771c2-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="771c2-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="771c2-132">輸入</span><span class="sxs-lookup"><span data-stu-id="771c2-132">INPUTS</span></span>

### <span data-ttu-id="771c2-133">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="771c2-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="771c2-134">System.object</span><span class="sxs-lookup"><span data-stu-id="771c2-134">System.String</span></span>

## <span data-ttu-id="771c2-135">輸出</span><span class="sxs-lookup"><span data-stu-id="771c2-135">OUTPUTS</span></span>

### <span data-ttu-id="771c2-136">PSConfiguration （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="771c2-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

### <span data-ttu-id="771c2-137">PSConfigurations []. IotHub. []</span><span class="sxs-lookup"><span data-stu-id="771c2-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurations[]</span></span>

## <span data-ttu-id="771c2-138">筆記</span><span class="sxs-lookup"><span data-stu-id="771c2-138">NOTES</span></span>

## <span data-ttu-id="771c2-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="771c2-139">RELATED LINKS</span></span>
