---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: 9ead4b38575bc297a820bda61eb6faf0beaf80d4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957109"
---
# <span data-ttu-id="dac23-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="dac23-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="dac23-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dac23-102">SYNOPSIS</span></span>
<span data-ttu-id="dac23-103">在虛擬機器上設定備份副檔名屬性。</span><span class="sxs-lookup"><span data-stu-id="dac23-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="dac23-104">句法</span><span class="sxs-lookup"><span data-stu-id="dac23-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dac23-105">說明</span><span class="sxs-lookup"><span data-stu-id="dac23-105">DESCRIPTION</span></span>

## <span data-ttu-id="dac23-106">示例</span><span class="sxs-lookup"><span data-stu-id="dac23-106">EXAMPLES</span></span>

### <span data-ttu-id="dac23-107">sr-1</span><span class="sxs-lookup"><span data-stu-id="dac23-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="dac23-108">參數</span><span class="sxs-lookup"><span data-stu-id="dac23-108">PARAMETERS</span></span>

### <span data-ttu-id="dac23-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dac23-109">-DefaultProfile</span></span>
<span data-ttu-id="dac23-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dac23-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dac23-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="dac23-111">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dac23-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dac23-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="dac23-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="dac23-113">-Tag</span></span>
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

### <span data-ttu-id="dac23-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="dac23-114">-VMName</span></span>
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

### <span data-ttu-id="dac23-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dac23-115">CommonParameters</span></span>
<span data-ttu-id="dac23-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dac23-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dac23-117">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dac23-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dac23-118">輸入</span><span class="sxs-lookup"><span data-stu-id="dac23-118">INPUTS</span></span>

### <span data-ttu-id="dac23-119">System.object</span><span class="sxs-lookup"><span data-stu-id="dac23-119">System.String</span></span>

## <span data-ttu-id="dac23-120">輸出</span><span class="sxs-lookup"><span data-stu-id="dac23-120">OUTPUTS</span></span>

### <span data-ttu-id="dac23-121">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="dac23-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="dac23-122">筆記</span><span class="sxs-lookup"><span data-stu-id="dac23-122">NOTES</span></span>

## <span data-ttu-id="dac23-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="dac23-123">RELATED LINKS</span></span>
