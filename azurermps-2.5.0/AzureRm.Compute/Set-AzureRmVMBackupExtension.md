---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbackupextension
schema: 2.0.0
ms.openlocfilehash: 5d31ad189dcc5337b81373d52a026e01f93f08a7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801338"
---
# <span data-ttu-id="c8bc3-101">Set-AzureRmVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="c8bc3-101">Set-AzureRmVMBackupExtension</span></span>

## <span data-ttu-id="c8bc3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8bc3-102">SYNOPSIS</span></span>
<span data-ttu-id="c8bc3-103">在虛擬機器上設定備份副檔名屬性。</span><span class="sxs-lookup"><span data-stu-id="c8bc3-103">Sets the backup extension properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8bc3-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8bc3-104">SYNTAX</span></span>

```
Set-AzureRmVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8bc3-105">說明</span><span class="sxs-lookup"><span data-stu-id="c8bc3-105">DESCRIPTION</span></span>

## <span data-ttu-id="c8bc3-106">示例</span><span class="sxs-lookup"><span data-stu-id="c8bc3-106">EXAMPLES</span></span>

### <span data-ttu-id="c8bc3-107">sr-1</span><span class="sxs-lookup"><span data-stu-id="c8bc3-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="c8bc3-108">參數</span><span class="sxs-lookup"><span data-stu-id="c8bc3-108">PARAMETERS</span></span>

### <span data-ttu-id="c8bc3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8bc3-109">-DefaultProfile</span></span>
<span data-ttu-id="c8bc3-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8bc3-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8bc3-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="c8bc3-111">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8bc3-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8bc3-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="c8bc3-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="c8bc3-113">-Tag</span></span>
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

### <span data-ttu-id="c8bc3-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="c8bc3-114">-VMName</span></span>
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

### <span data-ttu-id="c8bc3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8bc3-115">CommonParameters</span></span>
<span data-ttu-id="c8bc3-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8bc3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8bc3-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c8bc3-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8bc3-118">輸入</span><span class="sxs-lookup"><span data-stu-id="c8bc3-118">INPUTS</span></span>

### <span data-ttu-id="c8bc3-119">所有</span><span class="sxs-lookup"><span data-stu-id="c8bc3-119">None</span></span>
<span data-ttu-id="c8bc3-120">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="c8bc3-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c8bc3-121">輸出</span><span class="sxs-lookup"><span data-stu-id="c8bc3-121">OUTPUTS</span></span>

### <span data-ttu-id="c8bc3-122">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="c8bc3-122">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c8bc3-123">筆記</span><span class="sxs-lookup"><span data-stu-id="c8bc3-123">NOTES</span></span>

## <span data-ttu-id="c8bc3-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8bc3-124">RELATED LINKS</span></span>

