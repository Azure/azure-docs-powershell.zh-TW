---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryv2linkedserviceencryptedcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryV2LinkedServiceEncryptedCredential.md
ms.openlocfilehash: a99f7fbb1383d685a53cc11f9dd81f6f306ed633
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279298"
---
# <span data-ttu-id="ae749-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span><span class="sxs-lookup"><span data-stu-id="ae749-101">New-AzDataFactoryV2LinkedServiceEncryptedCredential</span></span>

## <span data-ttu-id="ae749-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ae749-102">SYNOPSIS</span></span>
<span data-ttu-id="ae749-103">在連結的服務中使用指定的整合執行時間來加密認證。</span><span class="sxs-lookup"><span data-stu-id="ae749-103">Encrypt credential in linked service with specified integration runtime.</span></span>

## <span data-ttu-id="ae749-104">句法</span><span class="sxs-lookup"><span data-stu-id="ae749-104">SYNTAX</span></span>

### <span data-ttu-id="ae749-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="ae749-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae749-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ae749-106">ByFactoryObject</span></span>
```
New-AzDataFactoryV2LinkedServiceEncryptedCredential [-IntegrationRuntimeName] <String>
 [-DefinitionFile] <String> [-Force] [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae749-107">說明</span><span class="sxs-lookup"><span data-stu-id="ae749-107">DESCRIPTION</span></span>
<span data-ttu-id="ae749-108">New-AzDataFactoryV2LinkedServiceEncryptedCredential Cmdlet 在連結的服務中使用指定的整合執行時間來加密認證。</span><span class="sxs-lookup"><span data-stu-id="ae749-108">The New-AzDataFactoryV2LinkedServiceEncryptedCredential cmdlet encrypt credential in linked service with specified integration runtime.</span></span>

<span data-ttu-id="ae749-109">請確定符合下列先決條件：</span><span class="sxs-lookup"><span data-stu-id="ae749-109">Please ensure the following prerequisites are met:</span></span>
* <span data-ttu-id="ae749-110">在自行託管的整合執行時間上啟用 **遠端存取** 選項。</span><span class="sxs-lookup"><span data-stu-id="ae749-110">**Remote access** option is enabled on the self-hosted integration runtime.</span></span>
* <span data-ttu-id="ae749-111">Powershell 7.0 或更新版本是用來執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ae749-111">Powershell 7.0 or higher is used to execute the cmdlet.</span></span>

## <span data-ttu-id="ae749-112">示例</span><span class="sxs-lookup"><span data-stu-id="ae749-112">EXAMPLES</span></span>

### <span data-ttu-id="ae749-113">範例1：加密連結服務中的認證</span><span class="sxs-lookup"><span data-stu-id="ae749-113">Example 1: Encrypt credentials in a linked service</span></span>

<span data-ttu-id="ae749-114">這個命令會利用名為 selfhost-ir 的整合執行時間，在檔案 C:\samples\WikiSample\TaxiDemo1.js中加密認證。</span><span class="sxs-lookup"><span data-stu-id="ae749-114">This command encrypts credential in file C:\samples\WikiSample\TaxiDemo1.json with the integration runtime named test-selfhost-ir.</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzDataFactoryV2LinkedServiceEncryptedCredential -DataFactoryName WikiADF -DefinitionFile 'C:\samples\WikiSample\TaxiDemo1.json' -IntegrationRuntimeName 'test-selfhost-ir' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="ae749-115">參數</span><span class="sxs-lookup"><span data-stu-id="ae749-115">PARAMETERS</span></span>

### <span data-ttu-id="ae749-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ae749-116">-DataFactory</span></span>
<span data-ttu-id="ae749-117">資料工廠物件。</span><span class="sxs-lookup"><span data-stu-id="ae749-117">The data factory object.</span></span>

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

### <span data-ttu-id="ae749-118">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ae749-118">-DataFactoryName</span></span>
<span data-ttu-id="ae749-119">資料工廠名稱。</span><span class="sxs-lookup"><span data-stu-id="ae749-119">The data factory name.</span></span>

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

### <span data-ttu-id="ae749-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae749-120">-DefaultProfile</span></span>
<span data-ttu-id="ae749-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae749-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae749-122">-DefinitionFile</span><span class="sxs-lookup"><span data-stu-id="ae749-122">-DefinitionFile</span></span>
<span data-ttu-id="ae749-123">JSON 檔路徑。</span><span class="sxs-lookup"><span data-stu-id="ae749-123">The JSON file path.</span></span>

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

### <span data-ttu-id="ae749-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ae749-124">-Force</span></span>
<span data-ttu-id="ae749-125">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ae749-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="ae749-126">-IntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="ae749-126">-IntegrationRuntimeName</span></span>
<span data-ttu-id="ae749-127">整合執行時間名稱。</span><span class="sxs-lookup"><span data-stu-id="ae749-127">The integration runtime name.</span></span>

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

### <span data-ttu-id="ae749-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae749-128">-ResourceGroupName</span></span>
<span data-ttu-id="ae749-129">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae749-129">The resource group name.</span></span>

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

### <span data-ttu-id="ae749-130">-確認</span><span class="sxs-lookup"><span data-stu-id="ae749-130">-Confirm</span></span>
<span data-ttu-id="ae749-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ae749-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae749-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae749-132">-WhatIf</span></span>
<span data-ttu-id="ae749-133">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ae749-133">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ae749-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae749-134">CommonParameters</span></span>
<span data-ttu-id="ae749-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ae749-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae749-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ae749-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae749-137">輸入</span><span class="sxs-lookup"><span data-stu-id="ae749-137">INPUTS</span></span>

### <span data-ttu-id="ae749-138">System.object</span><span class="sxs-lookup"><span data-stu-id="ae749-138">System.String</span></span>

### <span data-ttu-id="ae749-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ae749-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="ae749-140">輸出</span><span class="sxs-lookup"><span data-stu-id="ae749-140">OUTPUTS</span></span>

### <span data-ttu-id="ae749-141">System.object</span><span class="sxs-lookup"><span data-stu-id="ae749-141">System.String</span></span>

## <span data-ttu-id="ae749-142">筆記</span><span class="sxs-lookup"><span data-stu-id="ae749-142">NOTES</span></span>

## <span data-ttu-id="ae749-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae749-143">RELATED LINKS</span></span>
