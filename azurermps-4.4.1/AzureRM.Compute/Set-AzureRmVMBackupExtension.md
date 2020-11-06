---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBackupExtension.md
ms.openlocfilehash: d95ef152ed21439aafdc1cf9778b101473539b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445007"
---
# <span data-ttu-id="fdf3c-101">Set-AzureRmVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="fdf3c-101">Set-AzureRmVMBackupExtension</span></span>

## <span data-ttu-id="fdf3c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fdf3c-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf3c-103">在虛擬機器上設定備份副檔名屬性。</span><span class="sxs-lookup"><span data-stu-id="fdf3c-103">Sets the backup extension properties on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdf3c-104">句法</span><span class="sxs-lookup"><span data-stu-id="fdf3c-104">SYNTAX</span></span>

```
Set-AzureRmVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdf3c-105">說明</span><span class="sxs-lookup"><span data-stu-id="fdf3c-105">DESCRIPTION</span></span>

## <span data-ttu-id="fdf3c-106">示例</span><span class="sxs-lookup"><span data-stu-id="fdf3c-106">EXAMPLES</span></span>

### <span data-ttu-id="fdf3c-107">sr-1</span><span class="sxs-lookup"><span data-stu-id="fdf3c-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="fdf3c-108">參數</span><span class="sxs-lookup"><span data-stu-id="fdf3c-108">PARAMETERS</span></span>

### <span data-ttu-id="fdf3c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdf3c-109">-DefaultProfile</span></span>
<span data-ttu-id="fdf3c-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fdf3c-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fdf3c-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="fdf3c-111">-Name</span></span>
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

### <span data-ttu-id="fdf3c-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdf3c-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="fdf3c-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="fdf3c-113">-Tag</span></span>
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

### <span data-ttu-id="fdf3c-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="fdf3c-114">-VMName</span></span>
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

### <span data-ttu-id="fdf3c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf3c-115">CommonParameters</span></span>
<span data-ttu-id="fdf3c-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fdf3c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf3c-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fdf3c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf3c-118">輸入</span><span class="sxs-lookup"><span data-stu-id="fdf3c-118">INPUTS</span></span>

## <span data-ttu-id="fdf3c-119">輸出</span><span class="sxs-lookup"><span data-stu-id="fdf3c-119">OUTPUTS</span></span>

## <span data-ttu-id="fdf3c-120">筆記</span><span class="sxs-lookup"><span data-stu-id="fdf3c-120">NOTES</span></span>

## <span data-ttu-id="fdf3c-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="fdf3c-121">RELATED LINKS</span></span>

