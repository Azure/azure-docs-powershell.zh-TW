---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmDiskAccess.md
ms.openlocfilehash: 58cbbfd2314589fd6b28f2ff375aa268c39e63d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445035"
---
# <span data-ttu-id="a0865-101">Revoke-AzureRmDiskAccess</span><span class="sxs-lookup"><span data-stu-id="a0865-101">Revoke-AzureRmDiskAccess</span></span>

## <span data-ttu-id="a0865-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a0865-102">SYNOPSIS</span></span>
<span data-ttu-id="a0865-103">吊銷磁片存取權。</span><span class="sxs-lookup"><span data-stu-id="a0865-103">Revokes an access to a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0865-104">句法</span><span class="sxs-lookup"><span data-stu-id="a0865-104">SYNTAX</span></span>

```
Revoke-AzureRmDiskAccess [-ResourceGroupName] <String> [-DiskName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0865-105">說明</span><span class="sxs-lookup"><span data-stu-id="a0865-105">DESCRIPTION</span></span>
<span data-ttu-id="a0865-106">**Revoke AzureRmDiskAccess** Cmdlet 會吊銷磁片存取權。</span><span class="sxs-lookup"><span data-stu-id="a0865-106">The **Revoke-AzureRmDiskAccess** cmdlet revokes an access to a disk.</span></span>

## <span data-ttu-id="a0865-107">示例</span><span class="sxs-lookup"><span data-stu-id="a0865-107">EXAMPLES</span></span>

### <span data-ttu-id="a0865-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a0865-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="a0865-109">在名為 "ResourceGroup01" 的資源群組中，廢除名為「Disk01」的磁片存取權</span><span class="sxs-lookup"><span data-stu-id="a0865-109">Revoke the access to the disk named 'Disk01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="a0865-110">參數</span><span class="sxs-lookup"><span data-stu-id="a0865-110">PARAMETERS</span></span>

### <span data-ttu-id="a0865-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0865-111">-DefaultProfile</span></span>
<span data-ttu-id="a0865-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a0865-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0865-113">-DiskName</span><span class="sxs-lookup"><span data-stu-id="a0865-113">-DiskName</span></span>
<span data-ttu-id="a0865-114">指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0865-114">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="a0865-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0865-115">-ResourceGroupName</span></span>
<span data-ttu-id="a0865-116">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a0865-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a0865-117">-確認</span><span class="sxs-lookup"><span data-stu-id="a0865-117">-Confirm</span></span>
<span data-ttu-id="a0865-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a0865-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0865-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0865-119">-WhatIf</span></span>
<span data-ttu-id="a0865-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a0865-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a0865-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a0865-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0865-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0865-122">CommonParameters</span></span>
<span data-ttu-id="a0865-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a0865-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0865-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a0865-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0865-125">輸入</span><span class="sxs-lookup"><span data-stu-id="a0865-125">INPUTS</span></span>

### <span data-ttu-id="a0865-126">System.object</span><span class="sxs-lookup"><span data-stu-id="a0865-126">System.String</span></span>

## <span data-ttu-id="a0865-127">輸出</span><span class="sxs-lookup"><span data-stu-id="a0865-127">OUTPUTS</span></span>

### <span data-ttu-id="a0865-128">System.object</span><span class="sxs-lookup"><span data-stu-id="a0865-128">System.Object</span></span>

## <span data-ttu-id="a0865-129">筆記</span><span class="sxs-lookup"><span data-stu-id="a0865-129">NOTES</span></span>

## <span data-ttu-id="a0865-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="a0865-130">RELATED LINKS</span></span>

