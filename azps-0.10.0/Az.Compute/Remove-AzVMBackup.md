---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 2AB1B227-68C4-49AE-84C0-E1421E609DE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMBackup.md
ms.openlocfilehash: 02040fcb80fbf020b9d9dd3725369e75fbbf15c8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796049"
---
# <span data-ttu-id="85150-101">Remove-AzVMBackup</span><span class="sxs-lookup"><span data-stu-id="85150-101">Remove-AzVMBackup</span></span>

## <span data-ttu-id="85150-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85150-102">SYNOPSIS</span></span>
<span data-ttu-id="85150-103">從虛擬機器移除備份。</span><span class="sxs-lookup"><span data-stu-id="85150-103">Removes the backup from a virtual machine.</span></span>

## <span data-ttu-id="85150-104">句法</span><span class="sxs-lookup"><span data-stu-id="85150-104">SYNTAX</span></span>

```
Remove-AzVMBackup [-ResourceGroupName] <String> [-VMName] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85150-105">說明</span><span class="sxs-lookup"><span data-stu-id="85150-105">DESCRIPTION</span></span>

## <span data-ttu-id="85150-106">示例</span><span class="sxs-lookup"><span data-stu-id="85150-106">EXAMPLES</span></span>

### <span data-ttu-id="85150-107">sr-1</span><span class="sxs-lookup"><span data-stu-id="85150-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="85150-108">參數</span><span class="sxs-lookup"><span data-stu-id="85150-108">PARAMETERS</span></span>

### <span data-ttu-id="85150-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85150-109">-DefaultProfile</span></span>
<span data-ttu-id="85150-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="85150-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85150-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85150-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="85150-112">-Tag</span><span class="sxs-lookup"><span data-stu-id="85150-112">-Tag</span></span>
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

### <span data-ttu-id="85150-113">-VMName</span><span class="sxs-lookup"><span data-stu-id="85150-113">-VMName</span></span>
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

### <span data-ttu-id="85150-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85150-114">CommonParameters</span></span>
<span data-ttu-id="85150-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85150-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85150-116">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="85150-116">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85150-117">輸入</span><span class="sxs-lookup"><span data-stu-id="85150-117">INPUTS</span></span>

### <span data-ttu-id="85150-118">所有</span><span class="sxs-lookup"><span data-stu-id="85150-118">None</span></span>
<span data-ttu-id="85150-119">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="85150-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="85150-120">輸出</span><span class="sxs-lookup"><span data-stu-id="85150-120">OUTPUTS</span></span>

### <span data-ttu-id="85150-121">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="85150-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="85150-122">筆記</span><span class="sxs-lookup"><span data-stu-id="85150-122">NOTES</span></span>

## <span data-ttu-id="85150-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="85150-123">RELATED LINKS</span></span>

