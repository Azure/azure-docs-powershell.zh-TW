---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 5aeb8d7ba44f07519ff3cdfdc5e775687bd98260
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958908"
---
# <span data-ttu-id="ecf2e-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="ecf2e-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="ecf2e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ecf2e-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf2e-103">取得執行命令檔。</span><span class="sxs-lookup"><span data-stu-id="ecf2e-103">Get a run command document.</span></span>

## <span data-ttu-id="ecf2e-104">句法</span><span class="sxs-lookup"><span data-stu-id="ecf2e-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecf2e-105">說明</span><span class="sxs-lookup"><span data-stu-id="ecf2e-105">DESCRIPTION</span></span>
<span data-ttu-id="ecf2e-106">取得執行命令檔。</span><span class="sxs-lookup"><span data-stu-id="ecf2e-106">Get a run command document.</span></span>

## <span data-ttu-id="ecf2e-107">示例</span><span class="sxs-lookup"><span data-stu-id="ecf2e-107">EXAMPLES</span></span>

### <span data-ttu-id="ecf2e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ecf2e-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="ecf2e-109">在 "westus" 中取得「RunPowerShellScript」的特定執行命令檔。</span><span class="sxs-lookup"><span data-stu-id="ecf2e-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="ecf2e-110">範例2</span><span class="sxs-lookup"><span data-stu-id="ecf2e-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="ecf2e-111">列出 [westus] 中所有可用的 run 命令。</span><span class="sxs-lookup"><span data-stu-id="ecf2e-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="ecf2e-112">參數</span><span class="sxs-lookup"><span data-stu-id="ecf2e-112">PARAMETERS</span></span>

### <span data-ttu-id="ecf2e-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="ecf2e-113">-CommandId</span></span>
<span data-ttu-id="ecf2e-114">[命令識別碼]。</span><span class="sxs-lookup"><span data-stu-id="ecf2e-114">The command ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf2e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecf2e-115">-DefaultProfile</span></span>
<span data-ttu-id="ecf2e-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ecf2e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecf2e-117">-位置</span><span class="sxs-lookup"><span data-stu-id="ecf2e-117">-Location</span></span>
<span data-ttu-id="ecf2e-118">查詢執行命令的位置。</span><span class="sxs-lookup"><span data-stu-id="ecf2e-118">The location upon which run commands are queried.</span></span>

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

### <span data-ttu-id="ecf2e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf2e-119">CommonParameters</span></span>
<span data-ttu-id="ecf2e-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ecf2e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf2e-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ecf2e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf2e-122">輸入</span><span class="sxs-lookup"><span data-stu-id="ecf2e-122">INPUTS</span></span>

### <span data-ttu-id="ecf2e-123">System.object</span><span class="sxs-lookup"><span data-stu-id="ecf2e-123">System.String</span></span>

## <span data-ttu-id="ecf2e-124">輸出</span><span class="sxs-lookup"><span data-stu-id="ecf2e-124">OUTPUTS</span></span>

### <span data-ttu-id="ecf2e-125">PSRunCommandDocument 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="ecf2e-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="ecf2e-126">筆記</span><span class="sxs-lookup"><span data-stu-id="ecf2e-126">NOTES</span></span>

## <span data-ttu-id="ecf2e-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="ecf2e-127">RELATED LINKS</span></span>
