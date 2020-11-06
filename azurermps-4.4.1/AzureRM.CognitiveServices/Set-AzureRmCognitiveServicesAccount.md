---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 51338a2cae2aa8bde09ecdea18f0aa74f3727fef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456875"
---
# <span data-ttu-id="4b927-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4b927-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="4b927-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4b927-102">SYNOPSIS</span></span>
<span data-ttu-id="4b927-103">[修改帳戶]。</span><span class="sxs-lookup"><span data-stu-id="4b927-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b927-104">句法</span><span class="sxs-lookup"><span data-stu-id="4b927-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b927-105">說明</span><span class="sxs-lookup"><span data-stu-id="4b927-105">DESCRIPTION</span></span>
<span data-ttu-id="4b927-106">**AzureRmCognitiveServicesAccount** Cmdlet 會修改指定的認知服務帳戶的 SKU 或標記。</span><span class="sxs-lookup"><span data-stu-id="4b927-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="4b927-107">示例</span><span class="sxs-lookup"><span data-stu-id="4b927-107">EXAMPLES</span></span>

## <span data-ttu-id="4b927-108">參數</span><span class="sxs-lookup"><span data-stu-id="4b927-108">PARAMETERS</span></span>

### <span data-ttu-id="4b927-109">-Force</span><span class="sxs-lookup"><span data-stu-id="4b927-109">-Force</span></span>
<span data-ttu-id="4b927-110">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="4b927-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4b927-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="4b927-111">-Name</span></span>
<span data-ttu-id="4b927-112">指定要修改的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="4b927-112">Specifies the name of the account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b927-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b927-113">-ResourceGroupName</span></span>
<span data-ttu-id="4b927-114">指定將帳戶指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b927-114">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b927-115">-SkuName</span><span class="sxs-lookup"><span data-stu-id="4b927-115">-SkuName</span></span>
<span data-ttu-id="4b927-116">指定帳戶的 SKU。</span><span class="sxs-lookup"><span data-stu-id="4b927-116">Specifies the SKU for the account.</span></span>
<span data-ttu-id="4b927-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4b927-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4b927-118">F0 (自由層) </span><span class="sxs-lookup"><span data-stu-id="4b927-118">F0 (free tier)</span></span>
- <span data-ttu-id="4b927-119">S0</span><span class="sxs-lookup"><span data-stu-id="4b927-119">S0</span></span>
- <span data-ttu-id="4b927-120">S1</span><span class="sxs-lookup"><span data-stu-id="4b927-120">S1</span></span>
- <span data-ttu-id="4b927-121">S2</span><span class="sxs-lookup"><span data-stu-id="4b927-121">S2</span></span>
- <span data-ttu-id="4b927-122">S3</span><span class="sxs-lookup"><span data-stu-id="4b927-122">S3</span></span>
- <span data-ttu-id="4b927-123">喚醒</span><span class="sxs-lookup"><span data-stu-id="4b927-123">S4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b927-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="4b927-124">-Tag</span></span>
<span data-ttu-id="4b927-125">將標記指定為名稱/值對。</span><span class="sxs-lookup"><span data-stu-id="4b927-125">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b927-126">-確認</span><span class="sxs-lookup"><span data-stu-id="4b927-126">-Confirm</span></span>
<span data-ttu-id="4b927-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4b927-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b927-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b927-128">-WhatIf</span></span>
<span data-ttu-id="4b927-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4b927-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b927-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4b927-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b927-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b927-131">-DefaultProfile</span></span>
<span data-ttu-id="4b927-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4b927-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b927-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b927-133">CommonParameters</span></span>
<span data-ttu-id="4b927-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4b927-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b927-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4b927-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b927-136">輸入</span><span class="sxs-lookup"><span data-stu-id="4b927-136">INPUTS</span></span>

## <span data-ttu-id="4b927-137">輸出</span><span class="sxs-lookup"><span data-stu-id="4b927-137">OUTPUTS</span></span>

### <span data-ttu-id="4b927-138">PSCognitiveServicesAccount （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="4b927-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="4b927-139">筆記</span><span class="sxs-lookup"><span data-stu-id="4b927-139">NOTES</span></span>

## <span data-ttu-id="4b927-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b927-140">RELATED LINKS</span></span>

[<span data-ttu-id="4b927-141">AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4b927-141">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="4b927-142">新-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4b927-142">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="4b927-143">移除-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="4b927-143">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)
