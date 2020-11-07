---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzDisk.md
ms.openlocfilehash: 1da5ac8a6952e2a03367e84894f2069ba7ff250f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796313"
---
# <span data-ttu-id="42858-101">Get-AzDisk</span><span class="sxs-lookup"><span data-stu-id="42858-101">Get-AzDisk</span></span>

## <span data-ttu-id="42858-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42858-102">SYNOPSIS</span></span>
<span data-ttu-id="42858-103">取得受管理磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="42858-103">Gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="42858-104">句法</span><span class="sxs-lookup"><span data-stu-id="42858-104">SYNTAX</span></span>

```
Get-AzDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42858-105">說明</span><span class="sxs-lookup"><span data-stu-id="42858-105">DESCRIPTION</span></span>
<span data-ttu-id="42858-106">**AzDisk** Cmdlet 會取得受管理磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="42858-106">The **Get-AzDisk** cmdlet gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="42858-107">示例</span><span class="sxs-lookup"><span data-stu-id="42858-107">EXAMPLES</span></span>

### <span data-ttu-id="42858-108">範例1</span><span class="sxs-lookup"><span data-stu-id="42858-108">Example 1</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="42858-109">這個命令會取得資源群組 ' ResourceGroup01 ' 中名為 ' Disk01 ' 磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="42858-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="42858-110">範例2</span><span class="sxs-lookup"><span data-stu-id="42858-110">Example 2</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="42858-111">這個命令會取得資源群組 ' ResourceGroup01 ' 中所有磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="42858-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="42858-112">範例3</span><span class="sxs-lookup"><span data-stu-id="42858-112">Example 3</span></span>
```
PS C:\> Get-AzDisk
```

<span data-ttu-id="42858-113">這個命令會取得訂閱下所有磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="42858-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="42858-114">參數</span><span class="sxs-lookup"><span data-stu-id="42858-114">PARAMETERS</span></span>

### <span data-ttu-id="42858-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42858-115">-DefaultProfile</span></span>
<span data-ttu-id="42858-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="42858-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42858-117">-DiskName</span><span class="sxs-lookup"><span data-stu-id="42858-117">-DiskName</span></span>
<span data-ttu-id="42858-118">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="42858-118">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42858-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42858-119">-ResourceGroupName</span></span>
<span data-ttu-id="42858-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="42858-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42858-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42858-121">CommonParameters</span></span>
<span data-ttu-id="42858-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42858-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42858-123">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="42858-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42858-124">輸入</span><span class="sxs-lookup"><span data-stu-id="42858-124">INPUTS</span></span>

### <span data-ttu-id="42858-125">System.object</span><span class="sxs-lookup"><span data-stu-id="42858-125">System.String</span></span>

## <span data-ttu-id="42858-126">輸出</span><span class="sxs-lookup"><span data-stu-id="42858-126">OUTPUTS</span></span>

### <span data-ttu-id="42858-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="42858-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="42858-128">筆記</span><span class="sxs-lookup"><span data-stu-id="42858-128">NOTES</span></span>

## <span data-ttu-id="42858-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="42858-129">RELATED LINKS</span></span>

