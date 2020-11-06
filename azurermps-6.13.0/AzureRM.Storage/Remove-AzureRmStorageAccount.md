---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 006B4341-274C-4929-86EE-2E107BA9E485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccount.md
ms.openlocfilehash: 9c512c1993700e1bbdab4d5c0d52a1aa2ceeafb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455911"
---
# <span data-ttu-id="cd95e-101">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd95e-101">Remove-AzureRmStorageAccount</span></span>

## <span data-ttu-id="cd95e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cd95e-102">SYNOPSIS</span></span>
<span data-ttu-id="cd95e-103">從 Azure 移除儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="cd95e-103">Removes a Storage account from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd95e-104">句法</span><span class="sxs-lookup"><span data-stu-id="cd95e-104">SYNTAX</span></span>

```
Remove-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd95e-105">說明</span><span class="sxs-lookup"><span data-stu-id="cd95e-105">DESCRIPTION</span></span>
<span data-ttu-id="cd95e-106">**AzureRmStorageAccount** Cmdlet 會從 Azure 移除儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="cd95e-106">The **Remove-AzureRmStorageAccount** cmdlet removes a Storage account from Azure.</span></span>

## <span data-ttu-id="cd95e-107">示例</span><span class="sxs-lookup"><span data-stu-id="cd95e-107">EXAMPLES</span></span>

### <span data-ttu-id="cd95e-108">範例1：移除儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="cd95e-108">Example 1: Remove a Storage account</span></span>
```
PS C:\>Remove-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="cd95e-109">這個命令會移除指定的儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="cd95e-109">This command removes the specified Storage account.</span></span>

## <span data-ttu-id="cd95e-110">參數</span><span class="sxs-lookup"><span data-stu-id="cd95e-110">PARAMETERS</span></span>

### <span data-ttu-id="cd95e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd95e-111">-AsJob</span></span>
<span data-ttu-id="cd95e-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd95e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd95e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd95e-113">-DefaultProfile</span></span>
<span data-ttu-id="cd95e-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cd95e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd95e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cd95e-115">-Force</span></span>
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

### <span data-ttu-id="cd95e-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="cd95e-116">-Name</span></span>
<span data-ttu-id="cd95e-117">指定要移除的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="cd95e-117">Specifies the name of the Storage account to remove.</span></span>

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

### <span data-ttu-id="cd95e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd95e-118">-ResourceGroupName</span></span>
<span data-ttu-id="cd95e-119">指定包含要移除之儲存帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cd95e-119">Specifies the name of the resource group that contains the Storage account to remove.</span></span>

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

### <span data-ttu-id="cd95e-120">-確認</span><span class="sxs-lookup"><span data-stu-id="cd95e-120">-Confirm</span></span>
<span data-ttu-id="cd95e-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cd95e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd95e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd95e-122">-WhatIf</span></span>
<span data-ttu-id="cd95e-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cd95e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd95e-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cd95e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd95e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd95e-125">CommonParameters</span></span>
<span data-ttu-id="cd95e-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cd95e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd95e-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cd95e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd95e-128">輸入</span><span class="sxs-lookup"><span data-stu-id="cd95e-128">INPUTS</span></span>

### <span data-ttu-id="cd95e-129">System.object</span><span class="sxs-lookup"><span data-stu-id="cd95e-129">System.String</span></span>

## <span data-ttu-id="cd95e-130">輸出</span><span class="sxs-lookup"><span data-stu-id="cd95e-130">OUTPUTS</span></span>

### <span data-ttu-id="cd95e-131">System.void</span><span class="sxs-lookup"><span data-stu-id="cd95e-131">System.Void</span></span>

## <span data-ttu-id="cd95e-132">筆記</span><span class="sxs-lookup"><span data-stu-id="cd95e-132">NOTES</span></span>

## <span data-ttu-id="cd95e-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd95e-133">RELATED LINKS</span></span>

[<span data-ttu-id="cd95e-134">AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd95e-134">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="cd95e-135">新-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd95e-135">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="cd95e-136">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cd95e-136">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


