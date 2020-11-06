---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: 0fd40207f72f83c68418d0184922301e137ffc1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448457"
---
# <span data-ttu-id="11bad-101">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="11bad-101">Set-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="11bad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11bad-102">SYNOPSIS</span></span>
<span data-ttu-id="11bad-103">修改 Data Lake Store 中的檔案或資料夾擁有者。</span><span class="sxs-lookup"><span data-stu-id="11bad-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11bad-104">句法</span><span class="sxs-lookup"><span data-stu-id="11bad-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11bad-105">說明</span><span class="sxs-lookup"><span data-stu-id="11bad-105">DESCRIPTION</span></span>
<span data-ttu-id="11bad-106">**AzureRmDataLakeStoreItemOwner** Cmdlet 會修改 Data Lake store 中的檔案或資料夾擁有者。</span><span class="sxs-lookup"><span data-stu-id="11bad-106">The **Set-AzureRmDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="11bad-107">示例</span><span class="sxs-lookup"><span data-stu-id="11bad-107">EXAMPLES</span></span>

### <span data-ttu-id="11bad-108">範例1：設定專案的擁有者</span><span class="sxs-lookup"><span data-stu-id="11bad-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="11bad-109">這個命令會將根目錄的擁有者設定為 Patti 更完整的目錄。</span><span class="sxs-lookup"><span data-stu-id="11bad-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="11bad-110">參數</span><span class="sxs-lookup"><span data-stu-id="11bad-110">PARAMETERS</span></span>

### <span data-ttu-id="11bad-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="11bad-111">-Account</span></span>
<span data-ttu-id="11bad-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="11bad-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="11bad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11bad-113">-DefaultProfile</span></span>
<span data-ttu-id="11bad-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="11bad-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11bad-115">-識別碼</span><span class="sxs-lookup"><span data-stu-id="11bad-115">-Id</span></span>
<span data-ttu-id="11bad-116">指定要作為擁有者使用之 AzureActive 目錄使用者、群組或服務主體的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="11bad-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

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

### <span data-ttu-id="11bad-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11bad-117">-PassThru</span></span>
<span data-ttu-id="11bad-118">指出應該傳回所產生的更新擁有者。</span><span class="sxs-lookup"><span data-stu-id="11bad-118">Indicates the resulting updated owner should be returned.</span></span>

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

### <span data-ttu-id="11bad-119">-Path</span><span class="sxs-lookup"><span data-stu-id="11bad-119">-Path</span></span>
<span data-ttu-id="11bad-120">指定要修改之專案的 Data Lake Store 路徑（從根目錄 (/) 開始）。</span><span class="sxs-lookup"><span data-stu-id="11bad-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="11bad-121">-類型</span><span class="sxs-lookup"><span data-stu-id="11bad-121">-Type</span></span>
<span data-ttu-id="11bad-122">指定要設定的擁有者類型。</span><span class="sxs-lookup"><span data-stu-id="11bad-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="11bad-123">此參數可接受的值為： [使用者] 和 [群組]。</span><span class="sxs-lookup"><span data-stu-id="11bad-123">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="11bad-124">-確認</span><span class="sxs-lookup"><span data-stu-id="11bad-124">-Confirm</span></span>
<span data-ttu-id="11bad-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="11bad-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11bad-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11bad-126">-WhatIf</span></span>
<span data-ttu-id="11bad-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="11bad-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11bad-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="11bad-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11bad-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11bad-129">CommonParameters</span></span>
<span data-ttu-id="11bad-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11bad-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11bad-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="11bad-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11bad-132">輸入</span><span class="sxs-lookup"><span data-stu-id="11bad-132">INPUTS</span></span>

### <span data-ttu-id="11bad-133">System.object</span><span class="sxs-lookup"><span data-stu-id="11bad-133">System.String</span></span>

### <span data-ttu-id="11bad-134">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="11bad-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="11bad-135">DataLakeStoreEnums + 擁有者 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="11bad-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="11bad-136">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="11bad-136">System.Guid</span></span>

### <span data-ttu-id="11bad-137">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="11bad-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="11bad-138">輸出</span><span class="sxs-lookup"><span data-stu-id="11bad-138">OUTPUTS</span></span>

### <span data-ttu-id="11bad-139">System.object</span><span class="sxs-lookup"><span data-stu-id="11bad-139">System.Boolean</span></span>

## <span data-ttu-id="11bad-140">筆記</span><span class="sxs-lookup"><span data-stu-id="11bad-140">NOTES</span></span>

## <span data-ttu-id="11bad-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="11bad-141">RELATED LINKS</span></span>

[<span data-ttu-id="11bad-142">AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="11bad-142">Get-AzureRmDataLakeStoreItemOwner</span></span>](./Get-AzureRmDataLakeStoreItemOwner.md)


