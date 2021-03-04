---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 23ae31c79c33e9299d1cf3dc5998798657408da4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906945"
---
# <span data-ttu-id="a1949-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="a1949-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="a1949-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a1949-102">SYNOPSIS</span></span>
<span data-ttu-id="a1949-103">從虛擬機器移除備份。</span><span class="sxs-lookup"><span data-stu-id="a1949-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="a1949-104">語法</span><span class="sxs-lookup"><span data-stu-id="a1949-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1949-105">描述</span><span class="sxs-lookup"><span data-stu-id="a1949-105">DESCRIPTION</span></span>

## <span data-ttu-id="a1949-106">例子</span><span class="sxs-lookup"><span data-stu-id="a1949-106">EXAMPLES</span></span>

### <span data-ttu-id="a1949-107">1:</span><span class="sxs-lookup"><span data-stu-id="a1949-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="a1949-108">參數</span><span class="sxs-lookup"><span data-stu-id="a1949-108">PARAMETERS</span></span>

### <span data-ttu-id="a1949-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1949-109">-DefaultProfile</span></span>
<span data-ttu-id="a1949-110">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1949-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1949-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1949-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="a1949-112">-標記</span><span class="sxs-lookup"><span data-stu-id="a1949-112">-Tag</span></span>
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

### <span data-ttu-id="a1949-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="a1949-113">-VMName</span></span>
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

### <span data-ttu-id="a1949-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1949-114">CommonParameters</span></span>
<span data-ttu-id="a1949-115">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a1949-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1949-116">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1949-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1949-117">輸入</span><span class="sxs-lookup"><span data-stu-id="a1949-117">INPUTS</span></span>

### <span data-ttu-id="a1949-118">System.String</span><span class="sxs-lookup"><span data-stu-id="a1949-118">System.String</span></span>

## <span data-ttu-id="a1949-119">輸出</span><span class="sxs-lookup"><span data-stu-id="a1949-119">OUTPUTS</span></span>

### <span data-ttu-id="a1949-120">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a1949-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a1949-121">筆記</span><span class="sxs-lookup"><span data-stu-id="a1949-121">NOTES</span></span>

## <span data-ttu-id="a1949-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1949-122">RELATED LINKS</span></span>
