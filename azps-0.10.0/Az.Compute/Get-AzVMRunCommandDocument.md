---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 45d051e5fc2fe750f58dc6400a037960b7eb9c7c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796222"
---
# <span data-ttu-id="1379a-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="1379a-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="1379a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1379a-102">SYNOPSIS</span></span>
<span data-ttu-id="1379a-103">取得 [執行] 命令檔。</span><span class="sxs-lookup"><span data-stu-id="1379a-103">Get run command document.</span></span>

## <span data-ttu-id="1379a-104">句法</span><span class="sxs-lookup"><span data-stu-id="1379a-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1379a-105">說明</span><span class="sxs-lookup"><span data-stu-id="1379a-105">DESCRIPTION</span></span>
<span data-ttu-id="1379a-106">取得 [執行] 命令檔。</span><span class="sxs-lookup"><span data-stu-id="1379a-106">Get run command document.</span></span>

## <span data-ttu-id="1379a-107">示例</span><span class="sxs-lookup"><span data-stu-id="1379a-107">EXAMPLES</span></span>

### <span data-ttu-id="1379a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="1379a-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="1379a-109">在 "westus" 中取得「RunPowerShellScript」的特定執行命令檔。</span><span class="sxs-lookup"><span data-stu-id="1379a-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>


<span data-ttu-id="1379a-110">Get-AzVMRunCommandDocument 位置 $loc</span><span class="sxs-lookup"><span data-stu-id="1379a-110">Get-AzVMRunCommandDocument -Location $loc</span></span>

### <span data-ttu-id="1379a-111">範例2</span><span class="sxs-lookup"><span data-stu-id="1379a-111">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="1379a-112">列出 [westus] 中所有可用的 run 命令。</span><span class="sxs-lookup"><span data-stu-id="1379a-112">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="1379a-113">參數</span><span class="sxs-lookup"><span data-stu-id="1379a-113">PARAMETERS</span></span>

### <span data-ttu-id="1379a-114">-CommandId</span><span class="sxs-lookup"><span data-stu-id="1379a-114">-CommandId</span></span>
<span data-ttu-id="1379a-115">[命令識別碼]。</span><span class="sxs-lookup"><span data-stu-id="1379a-115">The command id.</span></span>

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

### <span data-ttu-id="1379a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1379a-116">-DefaultProfile</span></span>
<span data-ttu-id="1379a-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1379a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1379a-118">-位置</span><span class="sxs-lookup"><span data-stu-id="1379a-118">-Location</span></span>
<span data-ttu-id="1379a-119">查詢執行命令的位置。</span><span class="sxs-lookup"><span data-stu-id="1379a-119">The location upon which run commands is queried.</span></span>

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

### <span data-ttu-id="1379a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1379a-120">CommonParameters</span></span>
<span data-ttu-id="1379a-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1379a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1379a-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1379a-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1379a-123">輸入</span><span class="sxs-lookup"><span data-stu-id="1379a-123">INPUTS</span></span>

### <span data-ttu-id="1379a-124">System.object</span><span class="sxs-lookup"><span data-stu-id="1379a-124">System.String</span></span>

## <span data-ttu-id="1379a-125">輸出</span><span class="sxs-lookup"><span data-stu-id="1379a-125">OUTPUTS</span></span>

### <span data-ttu-id="1379a-126">PSRunCommandDocument 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="1379a-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="1379a-127">筆記</span><span class="sxs-lookup"><span data-stu-id="1379a-127">NOTES</span></span>

## <span data-ttu-id="1379a-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="1379a-128">RELATED LINKS</span></span>

