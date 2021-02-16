---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: 9ead4b38575bc297a820bda61eb6faf0beaf80d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136506"
---
# <span data-ttu-id="c9d33-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="c9d33-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="c9d33-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c9d33-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d33-103">在虛擬機器上設定備份副檔名屬性。</span><span class="sxs-lookup"><span data-stu-id="c9d33-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="c9d33-104">句法</span><span class="sxs-lookup"><span data-stu-id="c9d33-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9d33-105">說明</span><span class="sxs-lookup"><span data-stu-id="c9d33-105">DESCRIPTION</span></span>

## <span data-ttu-id="c9d33-106">示例</span><span class="sxs-lookup"><span data-stu-id="c9d33-106">EXAMPLES</span></span>

### <span data-ttu-id="c9d33-107">sr-1</span><span class="sxs-lookup"><span data-stu-id="c9d33-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="c9d33-108">參數</span><span class="sxs-lookup"><span data-stu-id="c9d33-108">PARAMETERS</span></span>

### <span data-ttu-id="c9d33-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d33-109">-DefaultProfile</span></span>
<span data-ttu-id="c9d33-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9d33-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9d33-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="c9d33-111">-Name</span></span>
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

### <span data-ttu-id="c9d33-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9d33-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="c9d33-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="c9d33-113">-Tag</span></span>
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

### <span data-ttu-id="c9d33-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="c9d33-114">-VMName</span></span>
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

### <span data-ttu-id="c9d33-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d33-115">CommonParameters</span></span>
<span data-ttu-id="c9d33-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c9d33-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d33-117">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c9d33-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d33-118">輸入</span><span class="sxs-lookup"><span data-stu-id="c9d33-118">INPUTS</span></span>

### <span data-ttu-id="c9d33-119">System.object</span><span class="sxs-lookup"><span data-stu-id="c9d33-119">System.String</span></span>

## <span data-ttu-id="c9d33-120">輸出</span><span class="sxs-lookup"><span data-stu-id="c9d33-120">OUTPUTS</span></span>

### <span data-ttu-id="c9d33-121">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="c9d33-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c9d33-122">筆記</span><span class="sxs-lookup"><span data-stu-id="c9d33-122">NOTES</span></span>

## <span data-ttu-id="c9d33-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9d33-123">RELATED LINKS</span></span>
