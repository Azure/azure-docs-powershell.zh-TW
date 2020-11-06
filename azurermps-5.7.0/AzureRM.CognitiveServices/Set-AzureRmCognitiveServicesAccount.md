---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/set-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Set-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: a31ee6979a73e4637e683a5b388f4265bf53d2a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455516"
---
# <span data-ttu-id="48eee-101">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="48eee-101">Set-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="48eee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="48eee-102">SYNOPSIS</span></span>
<span data-ttu-id="48eee-103">[修改帳戶]。</span><span class="sxs-lookup"><span data-stu-id="48eee-103">Modifies an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48eee-104">句法</span><span class="sxs-lookup"><span data-stu-id="48eee-104">SYNTAX</span></span>

```
Set-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="48eee-105">說明</span><span class="sxs-lookup"><span data-stu-id="48eee-105">DESCRIPTION</span></span>
<span data-ttu-id="48eee-106">**AzureRmCognitiveServicesAccount** Cmdlet 會修改指定的認知服務帳戶的 SKU 或標記。</span><span class="sxs-lookup"><span data-stu-id="48eee-106">The **Set-AzureRmCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="48eee-107">示例</span><span class="sxs-lookup"><span data-stu-id="48eee-107">EXAMPLES</span></span>

## <span data-ttu-id="48eee-108">參數</span><span class="sxs-lookup"><span data-stu-id="48eee-108">PARAMETERS</span></span>

### <span data-ttu-id="48eee-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48eee-109">-DefaultProfile</span></span>
<span data-ttu-id="48eee-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="48eee-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48eee-111">-Force</span><span class="sxs-lookup"><span data-stu-id="48eee-111">-Force</span></span>
<span data-ttu-id="48eee-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="48eee-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48eee-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="48eee-113">-Name</span></span>
<span data-ttu-id="48eee-114">指定要修改的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="48eee-114">Specifies the name of the account to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48eee-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48eee-115">-ResourceGroupName</span></span>
<span data-ttu-id="48eee-116">指定將帳戶指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="48eee-116">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48eee-117">-SkuName</span><span class="sxs-lookup"><span data-stu-id="48eee-117">-SkuName</span></span>
<span data-ttu-id="48eee-118">指定帳戶的 SKU。</span><span class="sxs-lookup"><span data-stu-id="48eee-118">Specifies the SKU for the account.</span></span>
<span data-ttu-id="48eee-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="48eee-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="48eee-120">F0 (自由層) </span><span class="sxs-lookup"><span data-stu-id="48eee-120">F0 (free tier)</span></span>
- <span data-ttu-id="48eee-121">S0</span><span class="sxs-lookup"><span data-stu-id="48eee-121">S0</span></span>
- <span data-ttu-id="48eee-122">S1</span><span class="sxs-lookup"><span data-stu-id="48eee-122">S1</span></span>
- <span data-ttu-id="48eee-123">S2</span><span class="sxs-lookup"><span data-stu-id="48eee-123">S2</span></span>
- <span data-ttu-id="48eee-124">S3</span><span class="sxs-lookup"><span data-stu-id="48eee-124">S3</span></span>
- <span data-ttu-id="48eee-125">喚醒</span><span class="sxs-lookup"><span data-stu-id="48eee-125">S4</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48eee-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="48eee-126">-Tag</span></span>
<span data-ttu-id="48eee-127">將標記指定為名稱/值對。</span><span class="sxs-lookup"><span data-stu-id="48eee-127">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48eee-128">-確認</span><span class="sxs-lookup"><span data-stu-id="48eee-128">-Confirm</span></span>
<span data-ttu-id="48eee-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="48eee-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48eee-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48eee-130">-WhatIf</span></span>
<span data-ttu-id="48eee-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="48eee-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48eee-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="48eee-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48eee-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48eee-133">CommonParameters</span></span>
<span data-ttu-id="48eee-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="48eee-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48eee-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="48eee-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48eee-136">輸入</span><span class="sxs-lookup"><span data-stu-id="48eee-136">INPUTS</span></span>

### <span data-ttu-id="48eee-137">所有</span><span class="sxs-lookup"><span data-stu-id="48eee-137">None</span></span>
<span data-ttu-id="48eee-138">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="48eee-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="48eee-139">輸出</span><span class="sxs-lookup"><span data-stu-id="48eee-139">OUTPUTS</span></span>

### <span data-ttu-id="48eee-140">PSCognitiveServicesAccount （CognitiveServices.）。</span><span class="sxs-lookup"><span data-stu-id="48eee-140">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="48eee-141">筆記</span><span class="sxs-lookup"><span data-stu-id="48eee-141">NOTES</span></span>

## <span data-ttu-id="48eee-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="48eee-142">RELATED LINKS</span></span>

[<span data-ttu-id="48eee-143">AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="48eee-143">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="48eee-144">新-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="48eee-144">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="48eee-145">移除-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="48eee-145">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)
