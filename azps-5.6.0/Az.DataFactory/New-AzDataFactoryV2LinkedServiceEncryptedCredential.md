---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 678cc7e015321d90fee5a5340caeeeb861b30600
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906713"
---
# <span data-ttu-id="3ef49-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="3ef49-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="3ef49-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3ef49-102">SYNOPSIS</span></span>
<span data-ttu-id="3ef49-103">使用指定的整合執行時間加密連結服務中的認證。</span><span class="sxs-lookup"><span data-stu-id="3ef49-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="3ef49-104">語法</span><span class="sxs-lookup"><span data-stu-id="3ef49-104">SYNTAX</span></span>

### <span data-ttu-id="3ef49-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="3ef49-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ef49-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="3ef49-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ef49-107">描述</span><span class="sxs-lookup"><span data-stu-id="3ef49-107">DESCRIPTION</span></span>
<span data-ttu-id="3ef49-108">此New-AzDataFactoryV2LinkedServiceEncryptedCredential Cmdlet 會使用指定的整合執行時間加密連結服務中的認證。</span><span class="sxs-lookup"><span data-stu-id="3ef49-108">The New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

<span data-ttu-id="3ef49-109">請確保符合下列先決條件：</span><span class="sxs-lookup"><span data-stu-id="3ef49-109">Please ensure the following prerequisites are met:</span></span>
* <span data-ttu-id="3ef49-110">**在自行託管** 的整合執行時間上啟用遠端存取選項。</span><span class="sxs-lookup"><span data-stu-id="3ef49-110">**Remote access** option is enabled on the self-hosted integration runtime.</span></span>
* <span data-ttu-id="3ef49-111">Powershell 7.0 或更高版本用來執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3ef49-111">Powershell 7.0 or higher is used to execute the cmdlet.</span></span>

## <span data-ttu-id="3ef49-112">例子</span><span class="sxs-lookup"><span data-stu-id="3ef49-112">EXAMPLES</span></span>

### <span data-ttu-id="3ef49-113">範例 1：加密連結服務中的認證</span><span class="sxs-lookup"><span data-stu-id="3ef49-113">Example 1: Encrypt credentials in a linked service</span></span>

<span data-ttu-id="3ef49-114">此命令會加密檔案中的認證C:\samples\WikiSample\TaxiDemo1.js名為 test-selfhost-ir 的整合執行時間。</span><span class="sxs-lookup"><span data-stu-id="3ef49-114">This command encrypts credential in file C:\samples\WikiSample\TaxiDemo1.json with the integration runtime named test-selfhost-ir.</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzDataFactoryV2LinkedServiceEncryptedCredential -DataFactoryName WikiADF -DefinitionFile 'C:\samples\WikiSample\TaxiDemo1.json' -IntegrationRuntimeName 'test-selfhost-ir' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="3ef49-115">參數</span><span class="sxs-lookup"><span data-stu-id="3ef49-115">PARAMETERS</span></span>

### <span data-ttu-id="3ef49-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="3ef49-116">-DataFactory</span></span>
<span data-ttu-id="3ef49-117">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="3ef49-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef49-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="3ef49-118">-DataFactoryName</span></span>
<span data-ttu-id="3ef49-119">資料出廠名稱。</span><span class="sxs-lookup"><span data-stu-id="3ef49-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef49-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ef49-120">-DefaultProfile</span></span>
<span data-ttu-id="3ef49-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3ef49-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ef49-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="3ef49-122">-DefinitionFile</span></span>
<span data-ttu-id="3ef49-123">JSON 檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="3ef49-123">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ef49-124">-強制</span><span class="sxs-lookup"><span data-stu-id="3ef49-124">-Force</span></span>
<span data-ttu-id="3ef49-125">執行 Cmdlet 而不提示確認。</span><span class="sxs-lookup"><span data-stu-id="3ef49-125">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ef49-126">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="3ef49-126">-IntegrationRuntimeName</span></span>
<span data-ttu-id="3ef49-127">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="3ef49-127">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef49-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ef49-128">-ResourceGroupName</span></span>
<span data-ttu-id="3ef49-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="3ef49-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ef49-130">-確認</span><span class="sxs-lookup"><span data-stu-id="3ef49-130">-Confirm</span></span>
<span data-ttu-id="3ef49-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3ef49-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ef49-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ef49-132">-WhatIf</span></span>
<span data-ttu-id="3ef49-133">顯示如果 Cmdlet 執行，但不執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3ef49-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ef49-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ef49-134">CommonParameters</span></span>
<span data-ttu-id="3ef49-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3ef49-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ef49-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3ef49-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ef49-137">輸入</span><span class="sxs-lookup"><span data-stu-id="3ef49-137">INPUTS</span></span>

### <span data-ttu-id="3ef49-138">System.String</span><span class="sxs-lookup"><span data-stu-id="3ef49-138">System.String</span></span>

### <span data-ttu-id="3ef49-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="3ef49-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="3ef49-140">輸出</span><span class="sxs-lookup"><span data-stu-id="3ef49-140">OUTPUTS</span></span>

### <span data-ttu-id="3ef49-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3ef49-141">System.String</span></span>

## <span data-ttu-id="3ef49-142">筆記</span><span class="sxs-lookup"><span data-stu-id="3ef49-142">NOTES</span></span>

## <span data-ttu-id="3ef49-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ef49-143">RELATED LINKS</span></span>
