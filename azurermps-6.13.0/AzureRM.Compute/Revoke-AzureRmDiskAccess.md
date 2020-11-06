---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/revoke-azurermdiskaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
ms.openlocfilehash: a0b6ddf2a5796c63c3efd20b811a2040db123836
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456127"
---
# <span data-ttu-id="dd3fd-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="dd3fd-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="dd3fd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dd3fd-102">SYNOPSIS</span></span>
<span data-ttu-id="dd3fd-103">吊銷磁片存取權。</span><span class="sxs-lookup"><span data-stu-id="dd3fd-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd3fd-104">句法</span><span class="sxs-lookup"><span data-stu-id="dd3fd-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd3fd-105">說明</span><span class="sxs-lookup"><span data-stu-id="dd3fd-105">DESCRIPTION</span></span>
<span data-ttu-id="dd3fd-106">**Revoke AzureRmDiskAccess** Cmdlet 會吊銷磁片存取權。</span><span class="sxs-lookup"><span data-stu-id="dd3fd-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="dd3fd-107">示例</span><span class="sxs-lookup"><span data-stu-id="dd3fd-107">EXAMPLES</span></span>

### <span data-ttu-id="dd3fd-108">範例1</span><span class="sxs-lookup"><span data-stu-id="dd3fd-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="dd3fd-109">在名為 "ResourceGroup01" 的資源群組中，廢除名為「Disk01」的磁片存取權</span><span class="sxs-lookup"><span data-stu-id="dd3fd-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="dd3fd-110">參數</span><span class="sxs-lookup"><span data-stu-id="dd3fd-110">PARAMETERS</span></span>

### <span data-ttu-id="dd3fd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dd3fd-111">-AsJob</span></span>
<span data-ttu-id="dd3fd-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dd3fd-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd3fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd3fd-113">-DefaultProfile</span></span>
<span data-ttu-id="dd3fd-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dd3fd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd3fd-115">-DiskName</span><span class="sxs-lookup"><span data-stu-id="dd3fd-115">-DiskName</span></span>
<span data-ttu-id="dd3fd-116">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd3fd-116">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd3fd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd3fd-117">-ResourceGroupName</span></span>
<span data-ttu-id="dd3fd-118">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd3fd-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd3fd-119">-確認</span><span class="sxs-lookup"><span data-stu-id="dd3fd-119">-Confirm</span></span>
<span data-ttu-id="dd3fd-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dd3fd-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd3fd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd3fd-121">-WhatIf</span></span>
<span data-ttu-id="dd3fd-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dd3fd-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dd3fd-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dd3fd-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd3fd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd3fd-124">CommonParameters</span></span>
<span data-ttu-id="dd3fd-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dd3fd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd3fd-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dd3fd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd3fd-127">輸入</span><span class="sxs-lookup"><span data-stu-id="dd3fd-127">INPUTS</span></span>

### <span data-ttu-id="dd3fd-128">System.object</span><span class="sxs-lookup"><span data-stu-id="dd3fd-128">System.String</span></span>

## <span data-ttu-id="dd3fd-129">輸出</span><span class="sxs-lookup"><span data-stu-id="dd3fd-129">OUTPUTS</span></span>

### <span data-ttu-id="dd3fd-130">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="dd3fd-130">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="dd3fd-131">筆記</span><span class="sxs-lookup"><span data-stu-id="dd3fd-131">NOTES</span></span>

## <span data-ttu-id="dd3fd-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="dd3fd-132">RELATED LINKS</span></span>
