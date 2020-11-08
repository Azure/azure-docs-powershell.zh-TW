---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 0ff9ef1337a1f2a5f0503c59dc4e6240d3c959b4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969326"
---
# <span data-ttu-id="0f469-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="0f469-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="0f469-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0f469-102">SYNOPSIS</span></span>
<span data-ttu-id="0f469-103">在連結的服務中使用指定的整合執行時間來加密認證。</span><span class="sxs-lookup"><span data-stu-id="0f469-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="0f469-104">句法</span><span class="sxs-lookup"><span data-stu-id="0f469-104">SYNTAX</span></span>

### <span data-ttu-id="0f469-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="0f469-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f469-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0f469-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f469-107">說明</span><span class="sxs-lookup"><span data-stu-id="0f469-107">DESCRIPTION</span></span>
<span data-ttu-id="0f469-108">New-AzDataFactoryV2LinkedServiceEncryptedCredential Cmdlet 在連結的服務中使用指定的整合執行時間來加密認證。</span><span class="sxs-lookup"><span data-stu-id="0f469-108">The New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="0f469-109">示例</span><span class="sxs-lookup"><span data-stu-id="0f469-109">EXAMPLES</span></span>

### <span data-ttu-id="0f469-110">範例1：加密連結服務中的認證</span><span class="sxs-lookup"><span data-stu-id="0f469-110">Example 1: Encrypt credentials in a linked service</span></span>

<span data-ttu-id="0f469-111">這個命令會利用名為 selfhost-ir 的整合執行時間，在檔案 C:\samples\WikiSample\TaxiDemo1.js中加密認證。</span><span class="sxs-lookup"><span data-stu-id="0f469-111">This command encrypts credential in file C:\samples\WikiSample\TaxiDemo1.json with the integration runtime named test-selfhost-ir.</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzDataFactoryV2LinkedServiceEncryptedCredential -DataFactoryName WikiADF -DefinitionFile 'C:\samples\WikiSample\TaxiDemo1.json' -IntegrationRuntimeName 'test-selfhost-ir' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="0f469-112">參數</span><span class="sxs-lookup"><span data-stu-id="0f469-112">PARAMETERS</span></span>

### <span data-ttu-id="0f469-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0f469-113">-DataFactory</span></span>
<span data-ttu-id="0f469-114">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="0f469-114">The data factory object.</span></span>

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

### <span data-ttu-id="0f469-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0f469-115">-DataFactoryName</span></span>
<span data-ttu-id="0f469-116">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="0f469-116">The data factory name.</span></span>

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

### <span data-ttu-id="0f469-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f469-117">-DefaultProfile</span></span>
<span data-ttu-id="0f469-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0f469-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f469-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="0f469-119">-DefinitionFile</span></span>
<span data-ttu-id="0f469-120">JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="0f469-120">The JSON file path.</span></span>

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

### <span data-ttu-id="0f469-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0f469-121">-Force</span></span>
<span data-ttu-id="0f469-122">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0f469-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0f469-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="0f469-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="0f469-124">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="0f469-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="0f469-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f469-125">-ResourceGroupName</span></span>
<span data-ttu-id="0f469-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0f469-126">The resource group name.</span></span>

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

### <span data-ttu-id="0f469-127">-確認</span><span class="sxs-lookup"><span data-stu-id="0f469-127">-Confirm</span></span>
<span data-ttu-id="0f469-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0f469-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f469-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f469-129">-WhatIf</span></span>
<span data-ttu-id="0f469-130">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0f469-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0f469-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f469-131">CommonParameters</span></span>
<span data-ttu-id="0f469-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0f469-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f469-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0f469-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f469-134">輸入</span><span class="sxs-lookup"><span data-stu-id="0f469-134">INPUTS</span></span>

### <span data-ttu-id="0f469-135">System.object</span><span class="sxs-lookup"><span data-stu-id="0f469-135">System.String</span></span>

### <span data-ttu-id="0f469-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0f469-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="0f469-137">輸出</span><span class="sxs-lookup"><span data-stu-id="0f469-137">OUTPUTS</span></span>

### <span data-ttu-id="0f469-138">System.object</span><span class="sxs-lookup"><span data-stu-id="0f469-138">System.String</span></span>

## <span data-ttu-id="0f469-139">筆記</span><span class="sxs-lookup"><span data-stu-id="0f469-139">NOTES</span></span>

## <span data-ttu-id="0f469-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f469-140">RELATED LINKS</span></span>
