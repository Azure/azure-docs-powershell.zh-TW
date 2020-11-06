---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 7bab6fb42e5d50cc0ede06a42540cf628a5ee4a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454895"
---
# <span data-ttu-id="e9b36-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="e9b36-101">Get-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="e9b36-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e9b36-102">SYNOPSIS</span></span>
<span data-ttu-id="e9b36-103">取得自託管整合執行時間的鍵。</span><span class="sxs-lookup"><span data-stu-id="e9b36-103">Gets keys for a self-hosted integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9b36-104">句法</span><span class="sxs-lookup"><span data-stu-id="e9b36-104">SYNTAX</span></span>

### <span data-ttu-id="e9b36-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="e9b36-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9b36-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e9b36-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9b36-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="e9b36-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9b36-108">說明</span><span class="sxs-lookup"><span data-stu-id="e9b36-108">DESCRIPTION</span></span>
<span data-ttu-id="e9b36-109">取得整合執行時間的金鑰。</span><span class="sxs-lookup"><span data-stu-id="e9b36-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="e9b36-110">金鑰是用來註冊整合執行時間節點。</span><span class="sxs-lookup"><span data-stu-id="e9b36-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="e9b36-111">示例</span><span class="sxs-lookup"><span data-stu-id="e9b36-111">EXAMPLES</span></span>

### <span data-ttu-id="e9b36-112">範例1：取得整合執行時間金鑰</span><span class="sxs-lookup"><span data-stu-id="e9b36-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="e9b36-113">這個 Cmdlet 會檢索名為「test-selfhost-ir」的整合執行時間的金鑰。</span><span class="sxs-lookup"><span data-stu-id="e9b36-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="e9b36-114">參數</span><span class="sxs-lookup"><span data-stu-id="e9b36-114">PARAMETERS</span></span>

### <span data-ttu-id="e9b36-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e9b36-115">-DataFactoryName</span></span>
<span data-ttu-id="e9b36-116">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="e9b36-116">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9b36-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9b36-117">-InputObject</span></span>
<span data-ttu-id="e9b36-118">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="e9b36-118">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9b36-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e9b36-119">-Name</span></span>
<span data-ttu-id="e9b36-120">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="e9b36-120">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9b36-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9b36-121">-ResourceGroupName</span></span>
<span data-ttu-id="e9b36-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9b36-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9b36-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9b36-123">-ResourceId</span></span>
<span data-ttu-id="e9b36-124">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e9b36-124">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9b36-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9b36-125">-DefaultProfile</span></span>
<span data-ttu-id="e9b36-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e9b36-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9b36-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9b36-127">CommonParameters</span></span>
<span data-ttu-id="e9b36-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e9b36-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9b36-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e9b36-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9b36-130">輸入</span><span class="sxs-lookup"><span data-stu-id="e9b36-130">INPUTS</span></span>

### <span data-ttu-id="e9b36-131">System.object</span><span class="sxs-lookup"><span data-stu-id="e9b36-131">System.String</span></span>
<span data-ttu-id="e9b36-132">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="e9b36-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span> 

## <span data-ttu-id="e9b36-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e9b36-133">OUTPUTS</span></span>

### <span data-ttu-id="e9b36-134">PSIntegrationRuntimeKeys 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="e9b36-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="e9b36-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e9b36-135">NOTES</span></span>

## <span data-ttu-id="e9b36-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9b36-136">RELATED LINKS</span></span>

[<span data-ttu-id="e9b36-137">新-AzureRmDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="e9b36-137">New-AzureRmDataFactoryV2IntegrationRuntimeKey</span></span>]()
