---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/revoke-azdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Revoke-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Revoke-AzDiskAccess.md
ms.openlocfilehash: 67c96d257be803e77555a7a93d8f9b1ebbbbf8c2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795977"
---
# <span data-ttu-id="0c3ab-101">Revoke-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="0c3ab-101">Revoke-AzDiskAccess</span></span>

## <span data-ttu-id="0c3ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0c3ab-102">SYNOPSIS</span></span>
<span data-ttu-id="0c3ab-103">吊銷磁片存取權。</span><span class="sxs-lookup"><span data-stu-id="0c3ab-103">Revokes an access to a disk.</span></span>

## <span data-ttu-id="0c3ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="0c3ab-104">SYNTAX</span></span>

```
Revoke-AzDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c3ab-105">說明</span><span class="sxs-lookup"><span data-stu-id="0c3ab-105">DESCRIPTION</span></span>
<span data-ttu-id="0c3ab-106">**Revoke AzDiskAccess** Cmdlet 會吊銷磁片存取權。</span><span class="sxs-lookup"><span data-stu-id="0c3ab-106">The **Revoke-AzDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="0c3ab-107">示例</span><span class="sxs-lookup"><span data-stu-id="0c3ab-107">EXAMPLES</span></span>

### <span data-ttu-id="0c3ab-108">範例1</span><span class="sxs-lookup"><span data-stu-id="0c3ab-108">Example 1</span></span>
```
PS C:\> Revoke-AzDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="0c3ab-109">在名為 "ResourceGroup01" 的資源群組中，廢除名為「Disk01」的磁片存取權</span><span class="sxs-lookup"><span data-stu-id="0c3ab-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="0c3ab-110">參數</span><span class="sxs-lookup"><span data-stu-id="0c3ab-110">PARAMETERS</span></span>

### <span data-ttu-id="0c3ab-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0c3ab-111">-AsJob</span></span>
<span data-ttu-id="0c3ab-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0c3ab-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c3ab-113">-DefaultProfile</span></span>
<span data-ttu-id="0c3ab-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0c3ab-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c3ab-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="0c3ab-115">-DiskName</span></span>
<span data-ttu-id="0c3ab-116">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c3ab-116">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3ab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c3ab-117">-ResourceGroupName</span></span>
<span data-ttu-id="0c3ab-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0c3ab-118">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c3ab-119">-確認</span><span class="sxs-lookup"><span data-stu-id="0c3ab-119">-Confirm</span></span>
<span data-ttu-id="0c3ab-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0c3ab-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3ab-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c3ab-121">-WhatIf</span></span>
<span data-ttu-id="0c3ab-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0c3ab-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c3ab-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c3ab-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c3ab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c3ab-124">CommonParameters</span></span>
<span data-ttu-id="0c3ab-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0c3ab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c3ab-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0c3ab-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c3ab-127">輸入</span><span class="sxs-lookup"><span data-stu-id="0c3ab-127">INPUTS</span></span>

### <span data-ttu-id="0c3ab-128">System.object</span><span class="sxs-lookup"><span data-stu-id="0c3ab-128">System.String</span></span>

## <span data-ttu-id="0c3ab-129">輸出</span><span class="sxs-lookup"><span data-stu-id="0c3ab-129">OUTPUTS</span></span>

### <span data-ttu-id="0c3ab-130">System.object</span><span class="sxs-lookup"><span data-stu-id="0c3ab-130">System.Object</span></span>

## <span data-ttu-id="0c3ab-131">筆記</span><span class="sxs-lookup"><span data-stu-id="0c3ab-131">NOTES</span></span>

## <span data-ttu-id="0c3ab-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c3ab-132">RELATED LINKS</span></span>

