---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: 37dbb1c81de0f7537dd708dc39b2356edfa46f6b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913222"
---
# <span data-ttu-id="b177d-101">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="b177d-101">Set-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="b177d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b177d-102">SYNOPSIS</span></span>
<span data-ttu-id="b177d-103">修改 Data Lake Store 中檔案或資料夾的擁有者。</span><span class="sxs-lookup"><span data-stu-id="b177d-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b177d-104">語法</span><span class="sxs-lookup"><span data-stu-id="b177d-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b177d-105">描述</span><span class="sxs-lookup"><span data-stu-id="b177d-105">DESCRIPTION</span></span>
<span data-ttu-id="b177d-106">**Set-AzDataLakeStoreItem Ownerer Cmdlet** 會修改 Data Lake Store 中檔案或資料夾的擁有者。</span><span class="sxs-lookup"><span data-stu-id="b177d-106">The **Set-AzDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="b177d-107">例子</span><span class="sxs-lookup"><span data-stu-id="b177d-107">EXAMPLES</span></span>

### <span data-ttu-id="b177d-108">範例 1：設定專案的擁有者</span><span class="sxs-lookup"><span data-stu-id="b177d-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="b177d-109">此命令將根目錄的擁有者設定為帕提 Fuller。</span><span class="sxs-lookup"><span data-stu-id="b177d-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="b177d-110">參數</span><span class="sxs-lookup"><span data-stu-id="b177d-110">PARAMETERS</span></span>

### <span data-ttu-id="b177d-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="b177d-111">-Account</span></span>
<span data-ttu-id="b177d-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b177d-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b177d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b177d-113">-DefaultProfile</span></span>
<span data-ttu-id="b177d-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b177d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b177d-115">-Id</span><span class="sxs-lookup"><span data-stu-id="b177d-115">-Id</span></span>
<span data-ttu-id="b177d-116">指定 AzureActive Directory 使用者、群組或服務主體的物件識別碼，以做為擁有者。</span><span class="sxs-lookup"><span data-stu-id="b177d-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b177d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b177d-117">-PassThru</span></span>
<span data-ttu-id="b177d-118">表示應該會退回產生的更新擁有者。</span><span class="sxs-lookup"><span data-stu-id="b177d-118">Indicates the resulting updated owner should be returned.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b177d-119">-路徑</span><span class="sxs-lookup"><span data-stu-id="b177d-119">-Path</span></span>
<span data-ttu-id="b177d-120">指定要修改之專案的 Data Lake Store 路徑，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="b177d-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b177d-121">-類型</span><span class="sxs-lookup"><span data-stu-id="b177d-121">-Type</span></span>
<span data-ttu-id="b177d-122">指定要設定之擁有者的類型。</span><span class="sxs-lookup"><span data-stu-id="b177d-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="b177d-123">此參數可接受的值為：使用者和群組。</span><span class="sxs-lookup"><span data-stu-id="b177d-123">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases:
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b177d-124">-確認</span><span class="sxs-lookup"><span data-stu-id="b177d-124">-Confirm</span></span>
<span data-ttu-id="b177d-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b177d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b177d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b177d-126">-WhatIf</span></span>
<span data-ttu-id="b177d-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b177d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b177d-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b177d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b177d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b177d-129">CommonParameters</span></span>
<span data-ttu-id="b177d-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b177d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b177d-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b177d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b177d-132">輸入</span><span class="sxs-lookup"><span data-stu-id="b177d-132">INPUTS</span></span>

### <span data-ttu-id="b177d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="b177d-133">System.String</span></span>

### <span data-ttu-id="b177d-134">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="b177d-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="b177d-135">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStoreEnums+Owner</span><span class="sxs-lookup"><span data-stu-id="b177d-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="b177d-136">System.Guid</span><span class="sxs-lookup"><span data-stu-id="b177d-136">System.Guid</span></span>

### <span data-ttu-id="b177d-137">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b177d-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b177d-138">輸出</span><span class="sxs-lookup"><span data-stu-id="b177d-138">OUTPUTS</span></span>

### <span data-ttu-id="b177d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b177d-139">System.String</span></span>

## <span data-ttu-id="b177d-140">筆記</span><span class="sxs-lookup"><span data-stu-id="b177d-140">NOTES</span></span>

## <span data-ttu-id="b177d-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="b177d-141">RELATED LINKS</span></span>

[<span data-ttu-id="b177d-142">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="b177d-142">Get-AzDataLakeStoreItemOwner</span></span>](./Get-AzDataLakeStoreItemOwner.md)


