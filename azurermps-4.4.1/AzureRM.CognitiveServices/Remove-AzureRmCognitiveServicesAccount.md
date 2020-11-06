---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Remove-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: a182bed0e93492521e3ac46d5f0ed3e2d705394c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456880"
---
# <span data-ttu-id="fa626-101">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fa626-101">Remove-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="fa626-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fa626-102">SYNOPSIS</span></span>
<span data-ttu-id="fa626-103">刪除認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="fa626-103">Deletes a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa626-104">句法</span><span class="sxs-lookup"><span data-stu-id="fa626-104">SYNTAX</span></span>

```
Remove-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa626-105">說明</span><span class="sxs-lookup"><span data-stu-id="fa626-105">DESCRIPTION</span></span>
<span data-ttu-id="fa626-106">**AzureRmCognitiveServicesAccount** Cmdlet 會刪除指定的認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="fa626-106">The **Remove-AzureRmCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="fa626-107">示例</span><span class="sxs-lookup"><span data-stu-id="fa626-107">EXAMPLES</span></span>

## <span data-ttu-id="fa626-108">參數</span><span class="sxs-lookup"><span data-stu-id="fa626-108">PARAMETERS</span></span>

### <span data-ttu-id="fa626-109">-Force</span><span class="sxs-lookup"><span data-stu-id="fa626-109">-Force</span></span>
<span data-ttu-id="fa626-110">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="fa626-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fa626-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="fa626-111">-Name</span></span>
<span data-ttu-id="fa626-112">指定要刪除的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="fa626-112">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="fa626-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa626-113">-ResourceGroupName</span></span>
<span data-ttu-id="fa626-114">指定將 [認知服務] 帳戶指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa626-114">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="fa626-115">-確認</span><span class="sxs-lookup"><span data-stu-id="fa626-115">-Confirm</span></span>
<span data-ttu-id="fa626-116">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fa626-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa626-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa626-117">-WhatIf</span></span>
<span data-ttu-id="fa626-118">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fa626-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa626-119">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fa626-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa626-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa626-120">-DefaultProfile</span></span>
<span data-ttu-id="fa626-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fa626-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa626-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa626-122">CommonParameters</span></span>
<span data-ttu-id="fa626-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fa626-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa626-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fa626-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa626-125">輸入</span><span class="sxs-lookup"><span data-stu-id="fa626-125">INPUTS</span></span>

## <span data-ttu-id="fa626-126">輸出</span><span class="sxs-lookup"><span data-stu-id="fa626-126">OUTPUTS</span></span>

## <span data-ttu-id="fa626-127">筆記</span><span class="sxs-lookup"><span data-stu-id="fa626-127">NOTES</span></span>

## <span data-ttu-id="fa626-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa626-128">RELATED LINKS</span></span>

[<span data-ttu-id="fa626-129">AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fa626-129">Get-AzureRmCognitiveServicesAccount</span></span>](./Get-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="fa626-130">新-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fa626-130">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="fa626-131">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="fa626-131">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


