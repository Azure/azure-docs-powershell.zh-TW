---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e598c266f46815e7005c43e2d354ad8ece06efc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455868"
---
# <span data-ttu-id="d39d4-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="d39d4-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="d39d4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d39d4-102">SYNOPSIS</span></span>
<span data-ttu-id="d39d4-103">取得磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="d39d4-103">Gets the properties of a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d39d4-104">句法</span><span class="sxs-lookup"><span data-stu-id="d39d4-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d39d4-105">說明</span><span class="sxs-lookup"><span data-stu-id="d39d4-105">DESCRIPTION</span></span>
<span data-ttu-id="d39d4-106">**AzureRmDisk** Cmdlet 會取得磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="d39d4-106">The **Get-AzureRmDisk** cmdlet gets the properties of a disk.</span></span>

## <span data-ttu-id="d39d4-107">示例</span><span class="sxs-lookup"><span data-stu-id="d39d4-107">EXAMPLES</span></span>

### <span data-ttu-id="d39d4-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d39d4-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="d39d4-109">這個命令會取得資源群組 ' ResourceGroup01 ' 中名為 ' Disk01 ' 磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="d39d4-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="d39d4-110">範例2</span><span class="sxs-lookup"><span data-stu-id="d39d4-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="d39d4-111">這個命令會取得資源群組 ' ResourceGroup01 ' 中所有磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="d39d4-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="d39d4-112">範例3</span><span class="sxs-lookup"><span data-stu-id="d39d4-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="d39d4-113">這個命令會取得訂閱下所有磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="d39d4-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="d39d4-114">參數</span><span class="sxs-lookup"><span data-stu-id="d39d4-114">PARAMETERS</span></span>

### <span data-ttu-id="d39d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d39d4-115">-DefaultProfile</span></span>
<span data-ttu-id="d39d4-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d39d4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d39d4-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="d39d4-117">-DiskName</span></span>
<span data-ttu-id="d39d4-118">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="d39d4-118">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d39d4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d39d4-119">-ResourceGroupName</span></span>
<span data-ttu-id="d39d4-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d39d4-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d39d4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d39d4-121">CommonParameters</span></span>
<span data-ttu-id="d39d4-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d39d4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d39d4-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d39d4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d39d4-124">輸入</span><span class="sxs-lookup"><span data-stu-id="d39d4-124">INPUTS</span></span>

### <span data-ttu-id="d39d4-125">System.object</span><span class="sxs-lookup"><span data-stu-id="d39d4-125">System.String</span></span>

## <span data-ttu-id="d39d4-126">輸出</span><span class="sxs-lookup"><span data-stu-id="d39d4-126">OUTPUTS</span></span>

### <span data-ttu-id="d39d4-127">System.object</span><span class="sxs-lookup"><span data-stu-id="d39d4-127">System.Object</span></span>

## <span data-ttu-id="d39d4-128">筆記</span><span class="sxs-lookup"><span data-stu-id="d39d4-128">NOTES</span></span>

## <span data-ttu-id="d39d4-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="d39d4-129">RELATED LINKS</span></span>

