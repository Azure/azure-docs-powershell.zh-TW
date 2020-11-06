---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 9bad5e162aaba3b1d1ffb0326a1b919420df18c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452511"
---
# <span data-ttu-id="84b3d-101">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="84b3d-101">Remove-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="84b3d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="84b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="84b3d-103">永久刪除 Data Lake Store 帳戶。</span><span class="sxs-lookup"><span data-stu-id="84b3d-103">Deletes a Data Lake Store account permanently.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84b3d-104">句法</span><span class="sxs-lookup"><span data-stu-id="84b3d-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84b3d-105">說明</span><span class="sxs-lookup"><span data-stu-id="84b3d-105">DESCRIPTION</span></span>
<span data-ttu-id="84b3d-106">**AzureRmDataLakeStoreAccount** Cmdlet 會將 [永久刪除 Data Lake store 帳戶]。</span><span class="sxs-lookup"><span data-stu-id="84b3d-106">The **Remove-AzureRmDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="84b3d-107">示例</span><span class="sxs-lookup"><span data-stu-id="84b3d-107">EXAMPLES</span></span>

### <span data-ttu-id="84b3d-108">範例1：移除資料 Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="84b3d-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="84b3d-109">這個命令會從 Data Lake Store 中移除名為 ContosoADL 的帳戶。</span><span class="sxs-lookup"><span data-stu-id="84b3d-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="84b3d-110">參數</span><span class="sxs-lookup"><span data-stu-id="84b3d-110">PARAMETERS</span></span>

### <span data-ttu-id="84b3d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="84b3d-111">-Force</span></span>
<span data-ttu-id="84b3d-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="84b3d-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="84b3d-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="84b3d-113">-Name</span></span>
<span data-ttu-id="84b3d-114">指定要移除的帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="84b3d-114">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="84b3d-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84b3d-115">-PassThru</span></span>
<span data-ttu-id="84b3d-116">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="84b3d-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="84b3d-117">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="84b3d-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="84b3d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84b3d-118">-ResourceGroupName</span></span>
<span data-ttu-id="84b3d-119">指定包含要移除之帳戶的資源群組。</span><span class="sxs-lookup"><span data-stu-id="84b3d-119">Specifies the resource group that contains the account to remove.</span></span>

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

### <span data-ttu-id="84b3d-120">-確認</span><span class="sxs-lookup"><span data-stu-id="84b3d-120">-Confirm</span></span>
<span data-ttu-id="84b3d-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="84b3d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84b3d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84b3d-122">-WhatIf</span></span>
<span data-ttu-id="84b3d-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="84b3d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84b3d-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="84b3d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84b3d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84b3d-125">-DefaultProfile</span></span>
<span data-ttu-id="84b3d-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="84b3d-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84b3d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84b3d-127">CommonParameters</span></span>
<span data-ttu-id="84b3d-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="84b3d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84b3d-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="84b3d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84b3d-130">輸入</span><span class="sxs-lookup"><span data-stu-id="84b3d-130">INPUTS</span></span>

## <span data-ttu-id="84b3d-131">輸出</span><span class="sxs-lookup"><span data-stu-id="84b3d-131">OUTPUTS</span></span>

### <span data-ttu-id="84b3d-132">bool</span><span class="sxs-lookup"><span data-stu-id="84b3d-132">bool</span></span>
<span data-ttu-id="84b3d-133">如果已指定 PassThru，則會在成功完成時傳回 true。</span><span class="sxs-lookup"><span data-stu-id="84b3d-133">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="84b3d-134">筆記</span><span class="sxs-lookup"><span data-stu-id="84b3d-134">NOTES</span></span>

## <span data-ttu-id="84b3d-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="84b3d-135">RELATED LINKS</span></span>

[<span data-ttu-id="84b3d-136">AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="84b3d-136">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="84b3d-137">新-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="84b3d-137">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="84b3d-138">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="84b3d-138">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="84b3d-139">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="84b3d-139">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


