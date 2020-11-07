---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmbackup
schema: 2.0.0
ms.openlocfilehash: 8805d5da061ef19037768b72c08145e45c8f2a9c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801706"
---
# <span data-ttu-id="7a94f-101">Remove-AzureRmVMBackup</span><span class="sxs-lookup"><span data-stu-id="7a94f-101">Remove-AzureRmVMBackup</span></span>

## <span data-ttu-id="7a94f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7a94f-102">SYNOPSIS</span></span>
<span data-ttu-id="7a94f-103">從虛擬機器移除備份。</span><span class="sxs-lookup"><span data-stu-id="7a94f-103">Removes the backup from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a94f-104">句法</span><span class="sxs-lookup"><span data-stu-id="7a94f-104">SYNTAX</span></span>

```
Remove-AzureRmVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a94f-105">說明</span><span class="sxs-lookup"><span data-stu-id="7a94f-105">DESCRIPTION</span></span>

## <span data-ttu-id="7a94f-106">示例</span><span class="sxs-lookup"><span data-stu-id="7a94f-106">EXAMPLES</span></span>

### <span data-ttu-id="7a94f-107">sr-1</span><span class="sxs-lookup"><span data-stu-id="7a94f-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="7a94f-108">參數</span><span class="sxs-lookup"><span data-stu-id="7a94f-108">PARAMETERS</span></span>

### <span data-ttu-id="7a94f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a94f-109">-DefaultProfile</span></span>
<span data-ttu-id="7a94f-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7a94f-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a94f-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a94f-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="7a94f-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="7a94f-112">-Tag</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a94f-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="7a94f-113">-VMName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a94f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a94f-114">CommonParameters</span></span>
<span data-ttu-id="7a94f-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7a94f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a94f-116">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7a94f-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a94f-117">輸入</span><span class="sxs-lookup"><span data-stu-id="7a94f-117">INPUTS</span></span>

### <span data-ttu-id="7a94f-118">所有</span><span class="sxs-lookup"><span data-stu-id="7a94f-118">None</span></span>
<span data-ttu-id="7a94f-119">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="7a94f-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7a94f-120">輸出</span><span class="sxs-lookup"><span data-stu-id="7a94f-120">OUTPUTS</span></span>

### <span data-ttu-id="7a94f-121">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="7a94f-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7a94f-122">筆記</span><span class="sxs-lookup"><span data-stu-id="7a94f-122">NOTES</span></span>

## <span data-ttu-id="7a94f-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="7a94f-123">RELATED LINKS</span></span>

