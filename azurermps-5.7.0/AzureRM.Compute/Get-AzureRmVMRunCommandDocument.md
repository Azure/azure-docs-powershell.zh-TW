---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMRunCommandDocument.md
ms.openlocfilehash: df53acc047ff0c17b3482f214c357f66ce638efb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625923"
---
# <span data-ttu-id="825cf-101">Get-AzureRmVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="825cf-101">Get-AzureRmVMRunCommandDocument</span></span>

## <span data-ttu-id="825cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="825cf-102">SYNOPSIS</span></span>
<span data-ttu-id="825cf-103">取得 [執行] 命令檔。</span><span class="sxs-lookup"><span data-stu-id="825cf-103">Get run command document.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="825cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="825cf-104">SYNTAX</span></span>

```
Get-AzureRmVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="825cf-105">說明</span><span class="sxs-lookup"><span data-stu-id="825cf-105">DESCRIPTION</span></span>
<span data-ttu-id="825cf-106">取得 [執行] 命令檔。</span><span class="sxs-lookup"><span data-stu-id="825cf-106">Get run command document.</span></span>

## <span data-ttu-id="825cf-107">示例</span><span class="sxs-lookup"><span data-stu-id="825cf-107">EXAMPLES</span></span>

### <span data-ttu-id="825cf-108">範例1</span><span class="sxs-lookup"><span data-stu-id="825cf-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="825cf-109">在 "westus" 中取得「RunPowerShellScript」的特定執行命令檔。</span><span class="sxs-lookup"><span data-stu-id="825cf-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="825cf-110">Get-AzureRmVMRunCommandDocument 位置 $loc</span><span class="sxs-lookup"><span data-stu-id="825cf-110">Get-AzureRmVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="825cf-111">範例2</span><span class="sxs-lookup"><span data-stu-id="825cf-111">Example 2</span></span>
```
PS C:\> Get-AzureRmVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="825cf-112">列出 [westus] 中所有可用的 run 命令。</span><span class="sxs-lookup"><span data-stu-id="825cf-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="825cf-113">參數</span><span class="sxs-lookup"><span data-stu-id="825cf-113">PARAMETERS</span></span>

### <span data-ttu-id="825cf-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="825cf-114">-CommandId</span></span>
<span data-ttu-id="825cf-115">[命令識別碼]。</span><span class="sxs-lookup"><span data-stu-id="825cf-115">The command id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="825cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="825cf-116">-DefaultProfile</span></span>
<span data-ttu-id="825cf-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="825cf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="825cf-118">-位置</span><span class="sxs-lookup"><span data-stu-id="825cf-118">-Location</span></span>
<span data-ttu-id="825cf-119">查詢執行命令的位置。</span><span class="sxs-lookup"><span data-stu-id="825cf-119">The location upon which run commands is queried.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="825cf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="825cf-120">CommonParameters</span></span>
<span data-ttu-id="825cf-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="825cf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="825cf-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="825cf-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="825cf-123">輸入</span><span class="sxs-lookup"><span data-stu-id="825cf-123">INPUTS</span></span>

### <span data-ttu-id="825cf-124">System.object</span><span class="sxs-lookup"><span data-stu-id="825cf-124">System.String</span></span>

## <span data-ttu-id="825cf-125">輸出</span><span class="sxs-lookup"><span data-stu-id="825cf-125">OUTPUTS</span></span>

### <span data-ttu-id="825cf-126">PSRunCommandDocument 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="825cf-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="825cf-127">筆記</span><span class="sxs-lookup"><span data-stu-id="825cf-127">NOTES</span></span>

## <span data-ttu-id="825cf-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="825cf-128">RELATED LINKS</span></span>
