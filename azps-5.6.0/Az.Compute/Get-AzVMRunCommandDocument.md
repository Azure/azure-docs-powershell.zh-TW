---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmruncommanddocument
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMRunCommandDocument.md
ms.openlocfilehash: 86d8e3bfebe8e87abacc78859dd6e776ff2ccf0b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909173"
---
# <span data-ttu-id="3eadc-101">Get-AzVMRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="3eadc-101">Get-AzVMRunCommandDocument</span></span>

## <span data-ttu-id="3eadc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3eadc-102">SYNOPSIS</span></span>
<span data-ttu-id="3eadc-103">取得執行命令檔。</span><span class="sxs-lookup"><span data-stu-id="3eadc-103">Get a run command document.</span></span>

## <span data-ttu-id="3eadc-104">語法</span><span class="sxs-lookup"><span data-stu-id="3eadc-104">SYNTAX</span></span>

```
Get-AzVMRunCommandDocument [-Location] <String> [[-CommandId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3eadc-105">描述</span><span class="sxs-lookup"><span data-stu-id="3eadc-105">DESCRIPTION</span></span>
<span data-ttu-id="3eadc-106">取得執行命令檔。</span><span class="sxs-lookup"><span data-stu-id="3eadc-106">Get a run command document.</span></span>

## <span data-ttu-id="3eadc-107">例子</span><span class="sxs-lookup"><span data-stu-id="3eadc-107">EXAMPLES</span></span>

### <span data-ttu-id="3eadc-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="3eadc-108">Example 1</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus' -CommandId 'RunPowerShellScript'
```

<span data-ttu-id="3eadc-109">在 "westus" 中為 "RunPowerShellScript" 獲得特定的執行命令檔。</span><span class="sxs-lookup"><span data-stu-id="3eadc-109">Gets a specific run command document for 'RunPowerShellScript' in 'westus'.</span></span>

### <span data-ttu-id="3eadc-110">範例 2</span><span class="sxs-lookup"><span data-stu-id="3eadc-110">Example 2</span></span>
```
PS C:\> Get-AzVMRunCommandDocument -Location 'westus'
```

<span data-ttu-id="3eadc-111">在 'westus' 中列出所有可用的執行命令。</span><span class="sxs-lookup"><span data-stu-id="3eadc-111">Lists all available run commands in 'westus'.</span></span>

## <span data-ttu-id="3eadc-112">參數</span><span class="sxs-lookup"><span data-stu-id="3eadc-112">PARAMETERS</span></span>

### <span data-ttu-id="3eadc-113">-CommandId</span><span class="sxs-lookup"><span data-stu-id="3eadc-113">-CommandId</span></span>
<span data-ttu-id="3eadc-114">命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="3eadc-114">The command ID.</span></span>

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

### <span data-ttu-id="3eadc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eadc-115">-DefaultProfile</span></span>
<span data-ttu-id="3eadc-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3eadc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3eadc-117">-位置</span><span class="sxs-lookup"><span data-stu-id="3eadc-117">-Location</span></span>
<span data-ttu-id="3eadc-118">查詢執行命令的位置。</span><span class="sxs-lookup"><span data-stu-id="3eadc-118">The location upon which run commands are queried.</span></span>

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

### <span data-ttu-id="3eadc-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eadc-119">CommonParameters</span></span>
<span data-ttu-id="3eadc-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3eadc-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eadc-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3eadc-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eadc-122">輸入</span><span class="sxs-lookup"><span data-stu-id="3eadc-122">INPUTS</span></span>

### <span data-ttu-id="3eadc-123">System.String</span><span class="sxs-lookup"><span data-stu-id="3eadc-123">System.String</span></span>

## <span data-ttu-id="3eadc-124">輸出</span><span class="sxs-lookup"><span data-stu-id="3eadc-124">OUTPUTS</span></span>

### <span data-ttu-id="3eadc-125">Microsoft.Azure.Commands.Compute.Automation.models.PSRunCommandDocument</span><span class="sxs-lookup"><span data-stu-id="3eadc-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSRunCommandDocument</span></span>

## <span data-ttu-id="3eadc-126">筆記</span><span class="sxs-lookup"><span data-stu-id="3eadc-126">NOTES</span></span>

## <span data-ttu-id="3eadc-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="3eadc-127">RELATED LINKS</span></span>
