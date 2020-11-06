---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: 765bd2c75a377204ab4566f47d0498deaf127953
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443916"
---
# <span data-ttu-id="b1601-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="b1601-101">New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="b1601-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b1601-102">SYNOPSIS</span></span>
<span data-ttu-id="b1601-103">在連結的服務中使用指定的整合執行時間來加密認證。</span><span class="sxs-lookup"><span data-stu-id="b1601-103">Encrypt credential in linked service with specified integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1601-104">句法</span><span class="sxs-lookup"><span data-stu-id="b1601-104">SYNTAX</span></span>

### <span data-ttu-id="b1601-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="b1601-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1601-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b1601-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1601-107">說明</span><span class="sxs-lookup"><span data-stu-id="b1601-107">DESCRIPTION</span></span>
<span data-ttu-id="b1601-108">New-AzureRmDataFactoryV2LinkedServiceEncryptCredential Cmdlet 在連結的服務中使用指定的整合執行時間來加密認證。</span><span class="sxs-lookup"><span data-stu-id="b1601-108">The New-AzureRmDataFactoryV2LinkedServiceEncryptCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="b1601-109">示例</span><span class="sxs-lookup"><span data-stu-id="b1601-109">EXAMPLES</span></span>

### <span data-ttu-id="b1601-110">範例1：在連結的服務中加密 creadentials</span><span class="sxs-lookup"><span data-stu-id="b1601-110">Example 1: Encrypt creadentials in a linked service</span></span>
```
PS C:\> New-AzureRmDataFactoryV2LinkedServiceEncryptCredential -ResourceGroupName resourceGroup -DataFactoryName myDataFactory -IntegrationRuntimeName myIR -File D:\sql.json
```

<span data-ttu-id="b1601-111">這個命令會使用名為 myIR 的整合執行時間，在檔案 D:\sql.js中加密認證。</span><span class="sxs-lookup"><span data-stu-id="b1601-111">This command encrypts credential in file D:\sql.json with the integration runtime named myIR.</span></span>

## <span data-ttu-id="b1601-112">參數</span><span class="sxs-lookup"><span data-stu-id="b1601-112">PARAMETERS</span></span>

### <span data-ttu-id="b1601-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b1601-113">-DataFactory</span></span>
<span data-ttu-id="b1601-114">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="b1601-114">The data factory object.</span></span>

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

### <span data-ttu-id="b1601-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b1601-115">-DataFactoryName</span></span>
<span data-ttu-id="b1601-116">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="b1601-116">The data factory name.</span></span>

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

### <span data-ttu-id="b1601-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1601-117">-DefaultProfile</span></span>
<span data-ttu-id="b1601-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1601-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1601-119">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="b1601-119">-DefinitionFile</span></span>
<span data-ttu-id="b1601-120">JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="b1601-120">The JSON file path.</span></span>

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

### <span data-ttu-id="b1601-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b1601-121">-Force</span></span>
<span data-ttu-id="b1601-122">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1601-122">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="b1601-123">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="b1601-123">-IntegrationRuntimeName</span></span>
<span data-ttu-id="b1601-124">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="b1601-124">The integration runtime name.</span></span>

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

### <span data-ttu-id="b1601-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1601-125">-ResourceGroupName</span></span>
<span data-ttu-id="b1601-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b1601-126">The resource group name.</span></span>

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

### <span data-ttu-id="b1601-127">-確認</span><span class="sxs-lookup"><span data-stu-id="b1601-127">-Confirm</span></span>
<span data-ttu-id="b1601-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b1601-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1601-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1601-129">-WhatIf</span></span>
<span data-ttu-id="b1601-130">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1601-130">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="b1601-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1601-131">CommonParameters</span></span>
<span data-ttu-id="b1601-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b1601-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1601-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b1601-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1601-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b1601-134">INPUTS</span></span>

### <span data-ttu-id="b1601-135">System.object</span><span class="sxs-lookup"><span data-stu-id="b1601-135">System.String</span></span>

### <span data-ttu-id="b1601-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b1601-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="b1601-137">參數： DataFactory (ByValue) </span><span class="sxs-lookup"><span data-stu-id="b1601-137">Parameters: DataFactory (ByValue)</span></span>

## <span data-ttu-id="b1601-138">輸出</span><span class="sxs-lookup"><span data-stu-id="b1601-138">OUTPUTS</span></span>

### <span data-ttu-id="b1601-139">System.object</span><span class="sxs-lookup"><span data-stu-id="b1601-139">System.String</span></span>

## <span data-ttu-id="b1601-140">筆記</span><span class="sxs-lookup"><span data-stu-id="b1601-140">NOTES</span></span>

## <span data-ttu-id="b1601-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1601-141">RELATED LINKS</span></span>