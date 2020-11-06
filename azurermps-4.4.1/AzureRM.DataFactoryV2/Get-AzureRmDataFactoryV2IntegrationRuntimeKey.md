---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: 42ccd34e299439d3288a8a587ce9d62abe198847
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456751"
---
# <span data-ttu-id="cba19-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="cba19-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="cba19-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cba19-102">SYNOPSIS</span></span>
<span data-ttu-id="cba19-103">取得自託管整合執行時間的鍵。</span><span class="sxs-lookup"><span data-stu-id="cba19-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cba19-104">句法</span><span class="sxs-lookup"><span data-stu-id="cba19-104">SYNTAX</span></span>

### <span data-ttu-id="cba19-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="cba19-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String>
```

### <span data-ttu-id="cba19-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cba19-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String>
```

### <span data-ttu-id="cba19-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="cba19-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
```

## <span data-ttu-id="cba19-108">說明</span><span class="sxs-lookup"><span data-stu-id="cba19-108">DESCRIPTION</span></span>
<span data-ttu-id="cba19-109">取得整合執行時間的金鑰。</span><span class="sxs-lookup"><span data-stu-id="cba19-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="cba19-110">金鑰是用來註冊整合執行時間節點。</span><span class="sxs-lookup"><span data-stu-id="cba19-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="cba19-111">示例</span><span class="sxs-lookup"><span data-stu-id="cba19-111">EXAMPLES</span></span>

### <span data-ttu-id="cba19-112">範例1：取得整合執行時間金鑰</span><span class="sxs-lookup"><span data-stu-id="cba19-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="cba19-113">這個 Cmdlet 會檢索名為「test-selfhost-ir」的整合執行時間的金鑰。</span><span class="sxs-lookup"><span data-stu-id="cba19-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="cba19-114">參數</span><span class="sxs-lookup"><span data-stu-id="cba19-114">PARAMETERS</span></span>

### <span data-ttu-id="cba19-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cba19-115">-DataFactoryName</span></span>
<span data-ttu-id="cba19-116">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="cba19-116">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba19-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cba19-117">-InputObject</span></span>
<span data-ttu-id="cba19-118">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="cba19-118">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cba19-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="cba19-119">-Name</span></span>
<span data-ttu-id="cba19-120">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="cba19-120">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba19-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cba19-121">-ResourceGroupName</span></span>
<span data-ttu-id="cba19-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cba19-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba19-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cba19-123">-ResourceId</span></span>
<span data-ttu-id="cba19-124">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="cba19-124">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="cba19-125">輸入</span><span class="sxs-lookup"><span data-stu-id="cba19-125">INPUTS</span></span>

### <span data-ttu-id="cba19-126">System.object</span><span class="sxs-lookup"><span data-stu-id="cba19-126">System.String</span></span>
<span data-ttu-id="cba19-127">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="cba19-127">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 


## <span data-ttu-id="cba19-128">輸出</span><span class="sxs-lookup"><span data-stu-id="cba19-128">OUTPUTS</span></span>

### <span data-ttu-id="cba19-129">PSIntegrationRuntimeKeys 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="cba19-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>


## <span data-ttu-id="cba19-130">筆記</span><span class="sxs-lookup"><span data-stu-id="cba19-130">NOTES</span></span>

## <span data-ttu-id="cba19-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="cba19-131">RELATED LINKS</span></span>
[<span data-ttu-id="cba19-132">新-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="cba19-132">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
