---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermdiskaccess
schema: 2.0.0
ms.openlocfilehash: f8da805a2c15356a4bf2188238b9a42a10617427
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800534"
---
# <span data-ttu-id="e5649-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="e5649-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="e5649-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5649-102">SYNOPSIS</span></span>
<span data-ttu-id="e5649-103">吊銷磁片存取權。</span><span class="sxs-lookup"><span data-stu-id="e5649-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5649-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5649-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5649-105">說明</span><span class="sxs-lookup"><span data-stu-id="e5649-105">DESCRIPTION</span></span>
<span data-ttu-id="e5649-106">**Revoke AzureRmDiskAccess** Cmdlet 會吊銷磁片存取權。</span><span class="sxs-lookup"><span data-stu-id="e5649-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="e5649-107">示例</span><span class="sxs-lookup"><span data-stu-id="e5649-107">EXAMPLES</span></span>

### <span data-ttu-id="e5649-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e5649-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="e5649-109">在名為 "ResourceGroup01" 的資源群組中，廢除名為「Disk01」的磁片存取權</span><span class="sxs-lookup"><span data-stu-id="e5649-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="e5649-110">參數</span><span class="sxs-lookup"><span data-stu-id="e5649-110">PARAMETERS</span></span>

### <span data-ttu-id="e5649-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5649-111">-AsJob</span></span>
<span data-ttu-id="e5649-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="e5649-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5649-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5649-113">-DefaultProfile</span></span>
<span data-ttu-id="e5649-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5649-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5649-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="e5649-115">-DiskName</span></span>
<span data-ttu-id="e5649-116">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5649-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="e5649-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5649-117">-ResourceGroupName</span></span>
<span data-ttu-id="e5649-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5649-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e5649-119">-確認</span><span class="sxs-lookup"><span data-stu-id="e5649-119">-Confirm</span></span>
<span data-ttu-id="e5649-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5649-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5649-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5649-121">-WhatIf</span></span>
<span data-ttu-id="e5649-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5649-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5649-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5649-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5649-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5649-124">CommonParameters</span></span>
<span data-ttu-id="e5649-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5649-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5649-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5649-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5649-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e5649-127">INPUTS</span></span>

### <span data-ttu-id="e5649-128">System.object</span><span class="sxs-lookup"><span data-stu-id="e5649-128">System.String</span></span>

## <span data-ttu-id="e5649-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e5649-129">OUTPUTS</span></span>

### <span data-ttu-id="e5649-130">System.object</span><span class="sxs-lookup"><span data-stu-id="e5649-130">System.Object</span></span>

## <span data-ttu-id="e5649-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e5649-131">NOTES</span></span>

## <span data-ttu-id="e5649-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5649-132">RELATED LINKS</span></span>

