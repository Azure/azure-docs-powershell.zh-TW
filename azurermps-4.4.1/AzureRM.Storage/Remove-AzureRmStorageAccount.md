---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
ms.openlocfilehash: ba63794844420accf2e5e664a43f74b2578c780d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624122"
---
# <span data-ttu-id="142ae-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="142ae-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="142ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="142ae-102">SYNOPSIS</span></span>
<span data-ttu-id="142ae-103">從 Azure 移除儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="142ae-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="142ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="142ae-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="142ae-105">說明</span><span class="sxs-lookup"><span data-stu-id="142ae-105">DESCRIPTION</span></span>
<span data-ttu-id="142ae-106">**AzureRmStorageAccount** Cmdlet 會從 Azure 移除儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="142ae-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="142ae-107">示例</span><span class="sxs-lookup"><span data-stu-id="142ae-107">EXAMPLES</span></span>

### <span data-ttu-id="142ae-108">範例1：移除儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="142ae-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="142ae-109">這個命令會移除指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="142ae-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="142ae-110">參數</span><span class="sxs-lookup"><span data-stu-id="142ae-110">PARAMETERS</span></span>

### <span data-ttu-id="142ae-111">-Force</span><span class="sxs-lookup"><span data-stu-id="142ae-111">-Force</span></span>
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

### <span data-ttu-id="142ae-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="142ae-112">-Name</span></span>
<span data-ttu-id="142ae-113">指定要移除的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="142ae-113">Specifies the name of the Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="142ae-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="142ae-114">-ResourceGroupName</span></span>
<span data-ttu-id="142ae-115">指定包含要移除之儲存帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="142ae-115">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="142ae-116">-確認</span><span class="sxs-lookup"><span data-stu-id="142ae-116">-Confirm</span></span>
<span data-ttu-id="142ae-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="142ae-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="142ae-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="142ae-118">-WhatIf</span></span>
<span data-ttu-id="142ae-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="142ae-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="142ae-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="142ae-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="142ae-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="142ae-121">-DefaultProfile</span></span>
<span data-ttu-id="142ae-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="142ae-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="142ae-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="142ae-123">CommonParameters</span></span>
<span data-ttu-id="142ae-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="142ae-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="142ae-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="142ae-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="142ae-126">輸入</span><span class="sxs-lookup"><span data-stu-id="142ae-126">INPUTS</span></span>

## <span data-ttu-id="142ae-127">輸出</span><span class="sxs-lookup"><span data-stu-id="142ae-127">OUTPUTS</span></span>

## <span data-ttu-id="142ae-128">筆記</span><span class="sxs-lookup"><span data-stu-id="142ae-128">NOTES</span></span>

## <span data-ttu-id="142ae-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="142ae-129">RELATED LINKS</span></span>

[<span data-ttu-id="142ae-130">AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="142ae-130">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="142ae-131">新-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="142ae-131">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="142ae-132">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="142ae-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


