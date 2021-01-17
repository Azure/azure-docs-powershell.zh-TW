---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 87A79215-5688-474D-822A-6B84B3D10E3F
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccount.md
ms.openlocfilehash: 1069365bb04cdf9a6d873e6fa86c61619b6d0dab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446547"
---
# <span data-ttu-id="857e3-101">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="857e3-101">Remove-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="857e3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="857e3-102">SYNOPSIS</span></span>
<span data-ttu-id="857e3-103">刪除認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="857e3-103">Deletes a Cognitive Services account.</span></span>

## <span data-ttu-id="857e3-104">句法</span><span class="sxs-lookup"><span data-stu-id="857e3-104">SYNTAX</span></span>

```
Remove-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="857e3-105">說明</span><span class="sxs-lookup"><span data-stu-id="857e3-105">DESCRIPTION</span></span>
<span data-ttu-id="857e3-106">**AzCognitiveServicesAccount** Cmdlet 會刪除指定的認知服務帳戶。</span><span class="sxs-lookup"><span data-stu-id="857e3-106">The **Remove-AzCognitiveServicesAccount** cmdlet deletes the specified Cognitive Services account.</span></span>

## <span data-ttu-id="857e3-107">示例</span><span class="sxs-lookup"><span data-stu-id="857e3-107">EXAMPLES</span></span>

### <span data-ttu-id="857e3-108">範例1</span><span class="sxs-lookup"><span data-stu-id="857e3-108">Example 1</span></span>
<span data-ttu-id="857e3-109">這個命令不會傳回任何內容。</span><span class="sxs-lookup"><span data-stu-id="857e3-109">This command doesn't return anything.</span></span>

```powershell
PS C:\> Remove-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis
PS C:\>
```

## <span data-ttu-id="857e3-110">參數</span><span class="sxs-lookup"><span data-stu-id="857e3-110">PARAMETERS</span></span>

### <span data-ttu-id="857e3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="857e3-111">-DefaultProfile</span></span>
<span data-ttu-id="857e3-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="857e3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="857e3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="857e3-113">-Force</span></span>
<span data-ttu-id="857e3-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="857e3-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="857e3-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="857e3-115">-Name</span></span>
<span data-ttu-id="857e3-116">指定要刪除的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="857e3-116">Specifies the name of the account to delete.</span></span>

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

### <span data-ttu-id="857e3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="857e3-117">-ResourceGroupName</span></span>
<span data-ttu-id="857e3-118">指定將 [認知服務] 帳戶指派給哪個資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="857e3-118">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

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

### <span data-ttu-id="857e3-119">-確認</span><span class="sxs-lookup"><span data-stu-id="857e3-119">-Confirm</span></span>
<span data-ttu-id="857e3-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="857e3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="857e3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="857e3-121">-WhatIf</span></span>
<span data-ttu-id="857e3-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="857e3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="857e3-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="857e3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="857e3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="857e3-124">CommonParameters</span></span>
<span data-ttu-id="857e3-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="857e3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="857e3-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="857e3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="857e3-127">輸入</span><span class="sxs-lookup"><span data-stu-id="857e3-127">INPUTS</span></span>

### <span data-ttu-id="857e3-128">System.object</span><span class="sxs-lookup"><span data-stu-id="857e3-128">System.String</span></span>

## <span data-ttu-id="857e3-129">輸出</span><span class="sxs-lookup"><span data-stu-id="857e3-129">OUTPUTS</span></span>

### <span data-ttu-id="857e3-130">System.void</span><span class="sxs-lookup"><span data-stu-id="857e3-130">System.Void</span></span>

## <span data-ttu-id="857e3-131">筆記</span><span class="sxs-lookup"><span data-stu-id="857e3-131">NOTES</span></span>

## <span data-ttu-id="857e3-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="857e3-132">RELATED LINKS</span></span>

[<span data-ttu-id="857e3-133">AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="857e3-133">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="857e3-134">新-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="857e3-134">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="857e3-135">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="857e3-135">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)


