---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeKey.md
ms.openlocfilehash: fc47b71b1546fe351f9d535da4ef9942af66f19e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907737"
---
# <span data-ttu-id="a3082-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="a3082-101">Get-AzDataFactoryV2IntegrationRuntimeKey</span></span>

## <span data-ttu-id="a3082-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a3082-102">SYNOPSIS</span></span>
<span data-ttu-id="a3082-103">獲得自我託管整合執行時間的金鑰。</span><span class="sxs-lookup"><span data-stu-id="a3082-103">Gets keys for a self-hosted integration runtime.</span></span>

## <span data-ttu-id="a3082-104">語法</span><span class="sxs-lookup"><span data-stu-id="a3082-104">SYNTAX</span></span>

### <span data-ttu-id="a3082-105">By方能RuntimeName (預設) </span><span class="sxs-lookup"><span data-stu-id="a3082-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3082-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a3082-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a3082-107">By方能RuntimeObject</span><span class="sxs-lookup"><span data-stu-id="a3082-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeKey [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3082-108">描述</span><span class="sxs-lookup"><span data-stu-id="a3082-108">DESCRIPTION</span></span>
<span data-ttu-id="a3082-109">取得整合執行時間的金鑰。</span><span class="sxs-lookup"><span data-stu-id="a3082-109">Get keys for an integration runtime.</span></span> <span data-ttu-id="a3082-110">這些金鑰是用來註冊整合執行時間節點。</span><span class="sxs-lookup"><span data-stu-id="a3082-110">The keys are used to register an integration runtime node.</span></span>

## <span data-ttu-id="a3082-111">例子</span><span class="sxs-lookup"><span data-stu-id="a3082-111">EXAMPLES</span></span>

### <span data-ttu-id="a3082-112">範例 1：取得整合執行時間金鑰</span><span class="sxs-lookup"><span data-stu-id="a3082-112">Example 1: Get integration runtime keys</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeKey -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir'

AuthKey1                                                 AuthKey2
--------                                                 --------
IR@89895504-f647-48fd-8dd3-42fa556d67e3******            IR@89895504-f647-48fd-8dd3-42fa556d67e3****
```

<span data-ttu-id="a3082-113">Cmdlet 會針對名為"test-selfhost-ir"的整合執行時間來取金鑰。</span><span class="sxs-lookup"><span data-stu-id="a3082-113">The cmdlet retrieves keys for an integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="a3082-114">參數</span><span class="sxs-lookup"><span data-stu-id="a3082-114">PARAMETERS</span></span>

### <span data-ttu-id="a3082-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a3082-115">-DataFactoryName</span></span>
<span data-ttu-id="a3082-116">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="a3082-116">The data factory name.</span></span>

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

### <span data-ttu-id="a3082-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3082-117">-DefaultProfile</span></span>
<span data-ttu-id="a3082-118">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a3082-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3082-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3082-119">-InputObject</span></span>
<span data-ttu-id="a3082-120">整合執行時間物件。</span><span class="sxs-lookup"><span data-stu-id="a3082-120">The integration runtime object.</span></span>

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

### <span data-ttu-id="a3082-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="a3082-121">-Name</span></span>
<span data-ttu-id="a3082-122">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="a3082-122">The integration runtime name.</span></span>

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

### <span data-ttu-id="a3082-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3082-123">-ResourceGroupName</span></span>
<span data-ttu-id="a3082-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="a3082-124">The resource group name.</span></span>

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

### <span data-ttu-id="a3082-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3082-125">-ResourceId</span></span>
<span data-ttu-id="a3082-126">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a3082-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a3082-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3082-127">CommonParameters</span></span>
<span data-ttu-id="a3082-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a3082-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3082-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a3082-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3082-130">輸入</span><span class="sxs-lookup"><span data-stu-id="a3082-130">INPUTS</span></span>

### <span data-ttu-id="a3082-131">System.String</span><span class="sxs-lookup"><span data-stu-id="a3082-131">System.String</span></span>

### <span data-ttu-id="a3082-132">Microsoft.Azure.Commands.DataFactoryV2.models.PSFactorRuntime</span><span class="sxs-lookup"><span data-stu-id="a3082-132">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="a3082-133">輸出</span><span class="sxs-lookup"><span data-stu-id="a3082-133">OUTPUTS</span></span>

### <span data-ttu-id="a3082-134">Microsoft.Azure.Commands.DataFactoryV2.models.PSFactorRuntimeKeys</span><span class="sxs-lookup"><span data-stu-id="a3082-134">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntimeKeys</span></span>

## <span data-ttu-id="a3082-135">筆記</span><span class="sxs-lookup"><span data-stu-id="a3082-135">NOTES</span></span>

## <span data-ttu-id="a3082-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3082-136">RELATED LINKS</span></span>

[<span data-ttu-id="a3082-137">New-AzDataFactoryV2FactoryRuntimeKey</span><span class="sxs-lookup"><span data-stu-id="a3082-137">New-AzDataFactoryV2IntegrationRuntimeKey</span></span>]()
