---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: 7be9116814af3f11e6bd61668b77df133676ab1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917346"
---
# <span data-ttu-id="f30a9-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="f30a9-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="f30a9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f30a9-102">SYNOPSIS</span></span>
<span data-ttu-id="f30a9-103">設定虛擬機器上的備份擴充功能屬性。</span><span class="sxs-lookup"><span data-stu-id="f30a9-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="f30a9-104">語法</span><span class="sxs-lookup"><span data-stu-id="f30a9-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f30a9-105">描述</span><span class="sxs-lookup"><span data-stu-id="f30a9-105">DESCRIPTION</span></span>

## <span data-ttu-id="f30a9-106">例子</span><span class="sxs-lookup"><span data-stu-id="f30a9-106">EXAMPLES</span></span>

### <span data-ttu-id="f30a9-107">1:</span><span class="sxs-lookup"><span data-stu-id="f30a9-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="f30a9-108">參數</span><span class="sxs-lookup"><span data-stu-id="f30a9-108">PARAMETERS</span></span>

### <span data-ttu-id="f30a9-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f30a9-109">-DefaultProfile</span></span>
<span data-ttu-id="f30a9-110">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f30a9-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f30a9-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="f30a9-111">-Name</span></span>
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

### <span data-ttu-id="f30a9-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f30a9-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="f30a9-113">-標記</span><span class="sxs-lookup"><span data-stu-id="f30a9-113">-Tag</span></span>
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

### <span data-ttu-id="f30a9-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="f30a9-114">-VMName</span></span>
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

### <span data-ttu-id="f30a9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f30a9-115">CommonParameters</span></span>
<span data-ttu-id="f30a9-116">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f30a9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f30a9-117">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f30a9-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f30a9-118">輸入</span><span class="sxs-lookup"><span data-stu-id="f30a9-118">INPUTS</span></span>

### <span data-ttu-id="f30a9-119">System.String</span><span class="sxs-lookup"><span data-stu-id="f30a9-119">System.String</span></span>

## <span data-ttu-id="f30a9-120">輸出</span><span class="sxs-lookup"><span data-stu-id="f30a9-120">OUTPUTS</span></span>

### <span data-ttu-id="f30a9-121">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f30a9-121">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f30a9-122">筆記</span><span class="sxs-lookup"><span data-stu-id="f30a9-122">NOTES</span></span>

## <span data-ttu-id="f30a9-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="f30a9-123">RELATED LINKS</span></span>
