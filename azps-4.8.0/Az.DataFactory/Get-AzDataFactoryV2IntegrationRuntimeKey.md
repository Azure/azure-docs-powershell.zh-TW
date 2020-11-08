---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: 6cfda34b1718cfd73108362ee81fbe9c638310c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136496"
---
# <span data-ttu-id="d65cf-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="d65cf-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="d65cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d65cf-102">SYNOPSIS</span></span>
<span data-ttu-id="d65cf-103">取得自託管整合執行時間的鍵。</span><span class="sxs-lookup"><span data-stu-id="d65cf-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="d65cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="d65cf-104">SYNTAX</span></span>

### <span data-ttu-id="d65cf-105">ByIntegrationRuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="d65cf-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d65cf-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d65cf-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d65cf-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="d65cf-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d65cf-108">說明</span><span class="sxs-lookup"><span data-stu-id="d65cf-108">DESCRIPTION</span></span>
<span data-ttu-id="d65cf-109">取得整合執行時間的金鑰。</span><span class="sxs-lookup"><span data-stu-id="d65cf-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="d65cf-110">金鑰是用來註冊整合執行時間節點。</span><span class="sxs-lookup"><span data-stu-id="d65cf-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="d65cf-111">示例</span><span class="sxs-lookup"><span data-stu-id="d65cf-111">EXAMPLES</span></span>

### <span data-ttu-id="d65cf-112">範例1：取得整合執行時間金鑰</span><span class="sxs-lookup"><span data-stu-id="d65cf-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="d65cf-113">這個 Cmdlet 會檢索名為「test-selfhost-ir」的整合執行時間的金鑰。</span><span class="sxs-lookup"><span data-stu-id="d65cf-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="d65cf-114">參數</span><span class="sxs-lookup"><span data-stu-id="d65cf-114">PARAMETERS</span></span>

### <span data-ttu-id="d65cf-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d65cf-115">-DataFactoryName</span></span>
<span data-ttu-id="d65cf-116">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="d65cf-116">The data factory name.</span></span>

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

### <span data-ttu-id="d65cf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d65cf-117">-DefaultProfile</span></span>
<span data-ttu-id="d65cf-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d65cf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d65cf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d65cf-119">-InputObject</span></span>
<span data-ttu-id="d65cf-120">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="d65cf-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="d65cf-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d65cf-121">-Name</span></span>
<span data-ttu-id="d65cf-122">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="d65cf-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="d65cf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d65cf-123">-ResourceGroupName</span></span>
<span data-ttu-id="d65cf-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d65cf-124">The resource group name.</span></span>

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

### <span data-ttu-id="d65cf-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d65cf-125">-ResourceId</span></span>
<span data-ttu-id="d65cf-126">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d65cf-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d65cf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d65cf-127">CommonParameters</span></span>
<span data-ttu-id="d65cf-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d65cf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d65cf-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d65cf-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d65cf-130">輸入</span><span class="sxs-lookup"><span data-stu-id="d65cf-130">INPUTS</span></span>

### <span data-ttu-id="d65cf-131">System.object</span><span class="sxs-lookup"><span data-stu-id="d65cf-131">System.String</span></span>

### <span data-ttu-id="d65cf-132">PSIntegrationRuntime 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="d65cf-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="d65cf-133">輸出</span><span class="sxs-lookup"><span data-stu-id="d65cf-133">OUTPUTS</span></span>

### <span data-ttu-id="d65cf-134">PSIntegrationRuntimeKeys 中的 DataFactoryV2。</span><span class="sxs-lookup"><span data-stu-id="d65cf-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="d65cf-135">筆記</span><span class="sxs-lookup"><span data-stu-id="d65cf-135">NOTES</span></span>

## <span data-ttu-id="d65cf-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="d65cf-136">RELATED LINKS</span></span>

[<span data-ttu-id="d65cf-137">新-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="d65cf-137">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
