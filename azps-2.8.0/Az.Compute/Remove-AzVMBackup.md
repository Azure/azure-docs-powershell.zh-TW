---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 1c2b58d58303dba38f907e9019f45502218c345a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613246"
---
# <span data-ttu-id="482f8-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="482f8-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="482f8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="482f8-102">SYNOPSIS</span></span>
<span data-ttu-id="482f8-103">從虛擬機器移除備份。</span><span class="sxs-lookup"><span data-stu-id="482f8-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="482f8-104">句法</span><span class="sxs-lookup"><span data-stu-id="482f8-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="482f8-105">說明</span><span class="sxs-lookup"><span data-stu-id="482f8-105">DESCRIPTION</span></span>

## <span data-ttu-id="482f8-106">示例</span><span class="sxs-lookup"><span data-stu-id="482f8-106">EXAMPLES</span></span>

### <span data-ttu-id="482f8-107">sr-1</span><span class="sxs-lookup"><span data-stu-id="482f8-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="482f8-108">參數</span><span class="sxs-lookup"><span data-stu-id="482f8-108">PARAMETERS</span></span>

### <span data-ttu-id="482f8-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="482f8-109">-DefaultProfile</span></span>
<span data-ttu-id="482f8-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="482f8-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="482f8-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="482f8-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="482f8-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="482f8-112">-Tag</span></span>
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

### <span data-ttu-id="482f8-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="482f8-113">-VMName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="482f8-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="482f8-114">CommonParameters</span></span>
<span data-ttu-id="482f8-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="482f8-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="482f8-116">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="482f8-116">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="482f8-117">輸入</span><span class="sxs-lookup"><span data-stu-id="482f8-117">INPUTS</span></span>

### <span data-ttu-id="482f8-118">System.object</span><span class="sxs-lookup"><span data-stu-id="482f8-118">System.String</span></span>

## <span data-ttu-id="482f8-119">輸出</span><span class="sxs-lookup"><span data-stu-id="482f8-119">OUTPUTS</span></span>

### <span data-ttu-id="482f8-120">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="482f8-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="482f8-121">筆記</span><span class="sxs-lookup"><span data-stu-id="482f8-121">NOTES</span></span>

## <span data-ttu-id="482f8-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="482f8-122">RELATED LINKS</span></span>
