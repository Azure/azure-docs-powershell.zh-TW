---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMBackup.md
ms.openlocfilehash: cb28249d5c32119d187becd8b07f2137f3f312d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623563"
---
# <span data-ttu-id="ef31f-101">Remove-AzureRmVMBackup</span><span class="sxs-lookup"><span data-stu-id="ef31f-101">Remove-AzureRmVMBackup</span></span>

## <span data-ttu-id="ef31f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef31f-102">SYNOPSIS</span></span>
<span data-ttu-id="ef31f-103">從虛擬機器移除備份。</span><span class="sxs-lookup"><span data-stu-id="ef31f-103">Removes the backup from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef31f-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef31f-104">SYNTAX</span></span>

```
Remove-AzureRmVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef31f-105">說明</span><span class="sxs-lookup"><span data-stu-id="ef31f-105">DESCRIPTION</span></span>

## <span data-ttu-id="ef31f-106">示例</span><span class="sxs-lookup"><span data-stu-id="ef31f-106">EXAMPLES</span></span>

### <span data-ttu-id="ef31f-107">sr-1</span><span class="sxs-lookup"><span data-stu-id="ef31f-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="ef31f-108">參數</span><span class="sxs-lookup"><span data-stu-id="ef31f-108">PARAMETERS</span></span>

### <span data-ttu-id="ef31f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef31f-109">-DefaultProfile</span></span>
<span data-ttu-id="ef31f-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef31f-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef31f-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef31f-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="ef31f-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="ef31f-112">-Tag</span></span>
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

### <span data-ttu-id="ef31f-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="ef31f-113">-VMName</span></span>
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

### <span data-ttu-id="ef31f-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef31f-114">CommonParameters</span></span>
<span data-ttu-id="ef31f-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef31f-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef31f-116">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ef31f-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef31f-117">輸入</span><span class="sxs-lookup"><span data-stu-id="ef31f-117">INPUTS</span></span>

### <span data-ttu-id="ef31f-118">System.object</span><span class="sxs-lookup"><span data-stu-id="ef31f-118">System.String</span></span>

## <span data-ttu-id="ef31f-119">輸出</span><span class="sxs-lookup"><span data-stu-id="ef31f-119">OUTPUTS</span></span>

### <span data-ttu-id="ef31f-120">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="ef31f-120">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ef31f-121">筆記</span><span class="sxs-lookup"><span data-stu-id="ef31f-121">NOTES</span></span>

## <span data-ttu-id="ef31f-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef31f-122">RELATED LINKS</span></span>
