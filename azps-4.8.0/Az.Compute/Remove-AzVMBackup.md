---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 85b7a873a921e7fd08055e1e3adc7c70831f8fa1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969849"
---
# <span data-ttu-id="b314e-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="b314e-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="b314e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b314e-102">SYNOPSIS</span></span>
<span data-ttu-id="b314e-103">從虛擬機器移除備份。</span><span class="sxs-lookup"><span data-stu-id="b314e-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="b314e-104">句法</span><span class="sxs-lookup"><span data-stu-id="b314e-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b314e-105">說明</span><span class="sxs-lookup"><span data-stu-id="b314e-105">DESCRIPTION</span></span>

## <span data-ttu-id="b314e-106">示例</span><span class="sxs-lookup"><span data-stu-id="b314e-106">EXAMPLES</span></span>

### <span data-ttu-id="b314e-107">sr-1</span><span class="sxs-lookup"><span data-stu-id="b314e-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="b314e-108">參數</span><span class="sxs-lookup"><span data-stu-id="b314e-108">PARAMETERS</span></span>

### <span data-ttu-id="b314e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b314e-109">-DefaultProfile</span></span>
<span data-ttu-id="b314e-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b314e-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b314e-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b314e-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="b314e-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="b314e-112">-Tag</span></span>
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

### <span data-ttu-id="b314e-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="b314e-113">-VMName</span></span>
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

### <span data-ttu-id="b314e-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b314e-114">CommonParameters</span></span>
<span data-ttu-id="b314e-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b314e-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b314e-116">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b314e-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b314e-117">輸入</span><span class="sxs-lookup"><span data-stu-id="b314e-117">INPUTS</span></span>

### <span data-ttu-id="b314e-118">System.object</span><span class="sxs-lookup"><span data-stu-id="b314e-118">System.String</span></span>

## <span data-ttu-id="b314e-119">輸出</span><span class="sxs-lookup"><span data-stu-id="b314e-119">OUTPUTS</span></span>

### <span data-ttu-id="b314e-120">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="b314e-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="b314e-121">筆記</span><span class="sxs-lookup"><span data-stu-id="b314e-121">NOTES</span></span>

## <span data-ttu-id="b314e-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="b314e-122">RELATED LINKS</span></span>
