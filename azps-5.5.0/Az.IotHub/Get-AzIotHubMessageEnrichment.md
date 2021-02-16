---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 91694efaeaf1a24018269706f3ee388feb7218ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131859"
---
# <span data-ttu-id="7e300-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="7e300-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="7e300-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7e300-102">SYNOPSIS</span></span>
<span data-ttu-id="7e300-103">為您的 IoT 中樞列出所有郵件 enrichments 或特定的郵件擴充。</span><span class="sxs-lookup"><span data-stu-id="7e300-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="7e300-104">句法</span><span class="sxs-lookup"><span data-stu-id="7e300-104">SYNTAX</span></span>

### <span data-ttu-id="7e300-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7e300-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e300-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7e300-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7e300-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7e300-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7e300-108">說明</span><span class="sxs-lookup"><span data-stu-id="7e300-108">DESCRIPTION</span></span>
<span data-ttu-id="7e300-109">如需 Azure IoT 中樞中郵件 enrichments 的詳細說明，請參閱 https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="7e300-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="7e300-110">示例</span><span class="sxs-lookup"><span data-stu-id="7e300-110">EXAMPLES</span></span>

### <span data-ttu-id="7e300-111">範例1</span><span class="sxs-lookup"><span data-stu-id="7e300-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="7e300-112">在 MyIotHub 中列出所有郵件 enrichments</span><span class="sxs-lookup"><span data-stu-id="7e300-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="7e300-113">範例2</span><span class="sxs-lookup"><span data-stu-id="7e300-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="7e300-114">顯示「newKey」訊息擴充的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="7e300-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="7e300-115">參數</span><span class="sxs-lookup"><span data-stu-id="7e300-115">PARAMETERS</span></span>

### <span data-ttu-id="7e300-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e300-116">-DefaultProfile</span></span>
<span data-ttu-id="7e300-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7e300-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e300-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e300-118">-InputObject</span></span>
<span data-ttu-id="7e300-119">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="7e300-119">IotHub object</span></span>

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

### <span data-ttu-id="7e300-120">-鍵</span><span class="sxs-lookup"><span data-stu-id="7e300-120">-Key</span></span>
<span data-ttu-id="7e300-121">擴充的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="7e300-121">The enrichment's key.</span></span>

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

### <span data-ttu-id="7e300-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="7e300-122">-Name</span></span>
<span data-ttu-id="7e300-123">Iot 中樞的名稱</span><span class="sxs-lookup"><span data-stu-id="7e300-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7e300-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e300-124">-ResourceGroupName</span></span>
<span data-ttu-id="7e300-125">資源群組的名稱</span><span class="sxs-lookup"><span data-stu-id="7e300-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7e300-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e300-126">-ResourceId</span></span>
<span data-ttu-id="7e300-127">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7e300-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7e300-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e300-128">CommonParameters</span></span>
<span data-ttu-id="7e300-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7e300-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e300-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7e300-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e300-131">輸入</span><span class="sxs-lookup"><span data-stu-id="7e300-131">INPUTS</span></span>

### <span data-ttu-id="7e300-132">PSIotHub （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="7e300-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7e300-133">System.object</span><span class="sxs-lookup"><span data-stu-id="7e300-133">System.String</span></span>

## <span data-ttu-id="7e300-134">輸出</span><span class="sxs-lookup"><span data-stu-id="7e300-134">OUTPUTS</span></span>

### <span data-ttu-id="7e300-135">PSEnrichmentMetadata （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="7e300-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="7e300-136">PSEnrichmentProperties []. IotHub. []</span><span class="sxs-lookup"><span data-stu-id="7e300-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="7e300-137">筆記</span><span class="sxs-lookup"><span data-stu-id="7e300-137">NOTES</span></span>

## <span data-ttu-id="7e300-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="7e300-138">RELATED LINKS</span></span>
