---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreAccount.md
ms.openlocfilehash: 8bb60e46f6785b29f8c2d64aadcce4d8697f4e16
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912026"
---
# <span data-ttu-id="03c44-101">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="03c44-101">Remove-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="03c44-102">簡介</span><span class="sxs-lookup"><span data-stu-id="03c44-102">SYNOPSIS</span></span>
<span data-ttu-id="03c44-103">永久刪除 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="03c44-103">Deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="03c44-104">語法</span><span class="sxs-lookup"><span data-stu-id="03c44-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03c44-105">描述</span><span class="sxs-lookup"><span data-stu-id="03c44-105">DESCRIPTION</span></span>
<span data-ttu-id="03c44-106">**Remove-AzDataLakeStoreAccount** Cmdlet 會永久刪除 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="03c44-106">The **Remove-AzDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="03c44-107">例子</span><span class="sxs-lookup"><span data-stu-id="03c44-107">EXAMPLES</span></span>

### <span data-ttu-id="03c44-108">範例 1：移除 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="03c44-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="03c44-109">此命令會從 Data Lake Store 移除名為 ContosoADL 的帳戶。</span><span class="sxs-lookup"><span data-stu-id="03c44-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="03c44-110">參數</span><span class="sxs-lookup"><span data-stu-id="03c44-110">PARAMETERS</span></span>

### <span data-ttu-id="03c44-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c44-111">-DefaultProfile</span></span>
<span data-ttu-id="03c44-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="03c44-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03c44-113">-強制</span><span class="sxs-lookup"><span data-stu-id="03c44-113">-Force</span></span>
<span data-ttu-id="03c44-114">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="03c44-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="03c44-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="03c44-115">-Name</span></span>
<span data-ttu-id="03c44-116">指定要移除的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="03c44-116">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="03c44-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03c44-117">-PassThru</span></span>
<span data-ttu-id="03c44-118">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="03c44-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="03c44-119">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="03c44-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="03c44-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03c44-120">-ResourceGroupName</span></span>
<span data-ttu-id="03c44-121">指定包含要移除之帳戶的資源群組。</span><span class="sxs-lookup"><span data-stu-id="03c44-121">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="03c44-122">-確認</span><span class="sxs-lookup"><span data-stu-id="03c44-122">-Confirm</span></span>
<span data-ttu-id="03c44-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="03c44-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03c44-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03c44-124">-WhatIf</span></span>
<span data-ttu-id="03c44-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="03c44-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03c44-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03c44-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03c44-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c44-127">CommonParameters</span></span>
<span data-ttu-id="03c44-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="03c44-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c44-129">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="03c44-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c44-130">輸入</span><span class="sxs-lookup"><span data-stu-id="03c44-130">INPUTS</span></span>

### <span data-ttu-id="03c44-131">System.String</span><span class="sxs-lookup"><span data-stu-id="03c44-131">System.String</span></span>

## <span data-ttu-id="03c44-132">輸出</span><span class="sxs-lookup"><span data-stu-id="03c44-132">OUTPUTS</span></span>

### <span data-ttu-id="03c44-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="03c44-133">System.Boolean</span></span>

## <span data-ttu-id="03c44-134">筆記</span><span class="sxs-lookup"><span data-stu-id="03c44-134">NOTES</span></span>

## <span data-ttu-id="03c44-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="03c44-135">RELATED LINKS</span></span>

[<span data-ttu-id="03c44-136">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="03c44-136">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="03c44-137">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="03c44-137">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="03c44-138">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="03c44-138">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="03c44-139">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="03c44-139">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


