---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
ms.openlocfilehash: 75af40b104bbf6ffa65211087572140a070b71e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136474"
---
# <span data-ttu-id="ff782-101">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ff782-101">Remove-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="ff782-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ff782-102">SYNOPSIS</span></span>
<span data-ttu-id="ff782-103">永久刪除 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="ff782-103">Deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="ff782-104">句法</span><span class="sxs-lookup"><span data-stu-id="ff782-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff782-105">說明</span><span class="sxs-lookup"><span data-stu-id="ff782-105">DESCRIPTION</span></span>
<span data-ttu-id="ff782-106">**AzDataLakeStoreAccount** Cmdlet 會將 [永久刪除 Data Lake store 帳戶]。</span><span class="sxs-lookup"><span data-stu-id="ff782-106">The **Remove-AzDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="ff782-107">示例</span><span class="sxs-lookup"><span data-stu-id="ff782-107">EXAMPLES</span></span>

### <span data-ttu-id="ff782-108">範例1：移除資料 Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="ff782-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="ff782-109">這個命令會從 Data Lake Store 中移除名為 ContosoADL 的帳戶。</span><span class="sxs-lookup"><span data-stu-id="ff782-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="ff782-110">參數</span><span class="sxs-lookup"><span data-stu-id="ff782-110">PARAMETERS</span></span>

### <span data-ttu-id="ff782-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff782-111">-DefaultProfile</span></span>
<span data-ttu-id="ff782-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ff782-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff782-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ff782-113">-Force</span></span>
<span data-ttu-id="ff782-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ff782-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff782-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="ff782-115">-Name</span></span>
<span data-ttu-id="ff782-116">指定要移除的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ff782-116">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="ff782-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff782-117">-PassThru</span></span>
<span data-ttu-id="ff782-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="ff782-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ff782-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="ff782-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff782-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff782-120">-ResourceGroupName</span></span>
<span data-ttu-id="ff782-121">指定包含要移除之帳戶的資源群組。</span><span class="sxs-lookup"><span data-stu-id="ff782-121">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="ff782-122">-確認</span><span class="sxs-lookup"><span data-stu-id="ff782-122">-Confirm</span></span>
<span data-ttu-id="ff782-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ff782-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff782-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff782-124">-WhatIf</span></span>
<span data-ttu-id="ff782-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ff782-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff782-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ff782-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff782-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff782-127">CommonParameters</span></span>
<span data-ttu-id="ff782-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ff782-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff782-129">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ff782-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff782-130">輸入</span><span class="sxs-lookup"><span data-stu-id="ff782-130">INPUTS</span></span>

### <span data-ttu-id="ff782-131">System.object</span><span class="sxs-lookup"><span data-stu-id="ff782-131">System.String</span></span>

## <span data-ttu-id="ff782-132">輸出</span><span class="sxs-lookup"><span data-stu-id="ff782-132">OUTPUTS</span></span>

### <span data-ttu-id="ff782-133">System.object</span><span class="sxs-lookup"><span data-stu-id="ff782-133">System.Boolean</span></span>

## <span data-ttu-id="ff782-134">筆記</span><span class="sxs-lookup"><span data-stu-id="ff782-134">NOTES</span></span>

## <span data-ttu-id="ff782-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff782-135">RELATED LINKS</span></span>

[<span data-ttu-id="ff782-136">AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ff782-136">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="ff782-137">新-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ff782-137">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="ff782-138">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ff782-138">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="ff782-139">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="ff782-139">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)

