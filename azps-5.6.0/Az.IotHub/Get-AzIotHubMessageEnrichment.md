---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubmessageenrichment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubMessageEnrichment.md
ms.openlocfilehash: 18a6d5db9ecf7cf02604a883b49545650413ee28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911042"
---
# <span data-ttu-id="10750-101">Get-AzIotHubMessageEnrichment</span><span class="sxs-lookup"><span data-stu-id="10750-101">Get-AzIotHubMessageEnrichment</span></span>

## <span data-ttu-id="10750-102">簡介</span><span class="sxs-lookup"><span data-stu-id="10750-102">SYNOPSIS</span></span>
<span data-ttu-id="10750-103">列出您的 IoT 中心的所有郵件擴充或特定郵件擴充。</span><span class="sxs-lookup"><span data-stu-id="10750-103">Lists all message enrichments or a particular message enrichment for your IoT Hub.</span></span>

## <span data-ttu-id="10750-104">語法</span><span class="sxs-lookup"><span data-stu-id="10750-104">SYNTAX</span></span>

### <span data-ttu-id="10750-105">ResourceSet (預設) </span><span class="sxs-lookup"><span data-stu-id="10750-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceGroupName] <String> [-Name] <String> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10750-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="10750-106">InputObjectSet</span></span>
```
Get-AzIotHubMessageEnrichment [-InputObject] <PSIotHub> [-Key <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10750-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="10750-107">ResourceIdSet</span></span>
```
Get-AzIotHubMessageEnrichment [-ResourceId] <String> [-Key <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="10750-108">描述</span><span class="sxs-lookup"><span data-stu-id="10750-108">DESCRIPTION</span></span>
<span data-ttu-id="10750-109">有關 Azure IoT Hub 中郵件擴充的詳細說明，請參閱 https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span><span class="sxs-lookup"><span data-stu-id="10750-109">For a detailed explanation of message enrichments in Azure IoT Hub, see https://docs.microsoft.com/azure/iot-hub/iot-hub-message-enrichments-overview</span></span>

## <span data-ttu-id="10750-110">例子</span><span class="sxs-lookup"><span data-stu-id="10750-110">EXAMPLES</span></span>

### <span data-ttu-id="10750-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="10750-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub"

Key  Value   Endpoint(s)
---  -----   -----------
key1 value1  {endpoint1, endpoint2}
key2 value2  {endpoint3, endpoint4}
```

<span data-ttu-id="10750-112">在 MyIotHub 中列出所有郵件擴充功能</span><span class="sxs-lookup"><span data-stu-id="10750-112">List all message enrichments in MyIotHub</span></span>

### <span data-ttu-id="10750-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="10750-113">Example 2</span></span>
```powershell
PS C:\>  Get-AzIotHubMessageEnrichment -ResourceGroupName "myresourcegroup" -Name "myiothub" -Key "newKey"

Key         : key1
Value       : value1
Endpoint(s) : {endpoint1, endpoint2}
```

<span data-ttu-id="10750-114">顯示有關「newKey」郵件擴充的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="10750-114">Show details about "newKey" message enrichment.</span></span>

## <span data-ttu-id="10750-115">參數</span><span class="sxs-lookup"><span data-stu-id="10750-115">PARAMETERS</span></span>

### <span data-ttu-id="10750-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10750-116">-DefaultProfile</span></span>
<span data-ttu-id="10750-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="10750-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10750-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10750-118">-InputObject</span></span>
<span data-ttu-id="10750-119">IotHub 物件</span><span class="sxs-lookup"><span data-stu-id="10750-119">IotHub object</span></span>

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

### <span data-ttu-id="10750-120">-Key</span><span class="sxs-lookup"><span data-stu-id="10750-120">-Key</span></span>
<span data-ttu-id="10750-121">這是擴充的關鍵。</span><span class="sxs-lookup"><span data-stu-id="10750-121">The enrichment's key.</span></span>

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

### <span data-ttu-id="10750-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="10750-122">-Name</span></span>
<span data-ttu-id="10750-123">Iot Hub 的名稱</span><span class="sxs-lookup"><span data-stu-id="10750-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="10750-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10750-124">-ResourceGroupName</span></span>
<span data-ttu-id="10750-125">資源組的名稱</span><span class="sxs-lookup"><span data-stu-id="10750-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="10750-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="10750-126">-ResourceId</span></span>
<span data-ttu-id="10750-127">IotHub 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="10750-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="10750-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10750-128">CommonParameters</span></span>
<span data-ttu-id="10750-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="10750-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10750-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="10750-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10750-131">輸入</span><span class="sxs-lookup"><span data-stu-id="10750-131">INPUTS</span></span>

### <span data-ttu-id="10750-132">Microsoft.Azure.Commands.management.IotHub.models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="10750-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="10750-133">System.String</span><span class="sxs-lookup"><span data-stu-id="10750-133">System.String</span></span>

## <span data-ttu-id="10750-134">輸出</span><span class="sxs-lookup"><span data-stu-id="10750-134">OUTPUTS</span></span>

### <span data-ttu-id="10750-135">Microsoft.Azure.Commands.management.IotHub.models.PSEn用mentMetadata</span><span class="sxs-lookup"><span data-stu-id="10750-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentMetadata</span></span>

### <span data-ttu-id="10750-136">Microsoft.Azure.Commands.management.IotHub.models.PSEntiesmentProperties[]</span><span class="sxs-lookup"><span data-stu-id="10750-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSEnrichmentProperties[]</span></span>

## <span data-ttu-id="10750-137">筆記</span><span class="sxs-lookup"><span data-stu-id="10750-137">NOTES</span></span>

## <span data-ttu-id="10750-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="10750-138">RELATED LINKS</span></span>
