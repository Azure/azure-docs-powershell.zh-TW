---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CBFFBF1B-1AF0-4D2F-9315-C3790A4E9346
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbackupextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBackupExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBackupExtension.md
ms.openlocfilehash: ce07d1a46fe0f13b18238d9e20fb1d4b28b7d861
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795898"
---
# <span data-ttu-id="498e5-101">Set-AzVMBackupExtension</span><span class="sxs-lookup"><span data-stu-id="498e5-101">Set-AzVMBackupExtension</span></span>

## <span data-ttu-id="498e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="498e5-102">SYNOPSIS</span></span>
<span data-ttu-id="498e5-103">在虛擬機器上設定備份副檔名屬性。</span><span class="sxs-lookup"><span data-stu-id="498e5-103">Sets the backup extension properties on a virtual machine.</span></span>

## <span data-ttu-id="498e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="498e5-104">SYNTAX</span></span>

```
Set-AzVMBackupExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Tag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="498e5-105">說明</span><span class="sxs-lookup"><span data-stu-id="498e5-105">DESCRIPTION</span></span>

## <span data-ttu-id="498e5-106">示例</span><span class="sxs-lookup"><span data-stu-id="498e5-106">EXAMPLES</span></span>

### <span data-ttu-id="498e5-107">sr-1</span><span class="sxs-lookup"><span data-stu-id="498e5-107">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="498e5-108">參數</span><span class="sxs-lookup"><span data-stu-id="498e5-108">PARAMETERS</span></span>

### <span data-ttu-id="498e5-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="498e5-109">-DefaultProfile</span></span>
<span data-ttu-id="498e5-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="498e5-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="498e5-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="498e5-111">-Name</span></span>
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

### <span data-ttu-id="498e5-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="498e5-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="498e5-113">-Tag</span><span class="sxs-lookup"><span data-stu-id="498e5-113">-Tag</span></span>
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

### <span data-ttu-id="498e5-114">-VMName</span><span class="sxs-lookup"><span data-stu-id="498e5-114">-VMName</span></span>
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

### <span data-ttu-id="498e5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="498e5-115">CommonParameters</span></span>
<span data-ttu-id="498e5-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="498e5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="498e5-117">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="498e5-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="498e5-118">輸入</span><span class="sxs-lookup"><span data-stu-id="498e5-118">INPUTS</span></span>

### <span data-ttu-id="498e5-119">所有</span><span class="sxs-lookup"><span data-stu-id="498e5-119">None</span></span>
<span data-ttu-id="498e5-120">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="498e5-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="498e5-121">輸出</span><span class="sxs-lookup"><span data-stu-id="498e5-121">OUTPUTS</span></span>

### <span data-ttu-id="498e5-122">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="498e5-122">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="498e5-123">筆記</span><span class="sxs-lookup"><span data-stu-id="498e5-123">NOTES</span></span>

## <span data-ttu-id="498e5-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="498e5-124">RELATED LINKS</span></span>

