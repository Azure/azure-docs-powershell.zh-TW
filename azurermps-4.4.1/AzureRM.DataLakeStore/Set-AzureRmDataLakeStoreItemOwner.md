---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: fc71ec338303876a2cff44a07632e9fae5d3d2d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626627"
---
# <span data-ttu-id="67db2-101">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="67db2-101">Set-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="67db2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="67db2-102">SYNOPSIS</span></span>
<span data-ttu-id="67db2-103">修改 Data Lake Store 中的檔案或資料夾擁有者。</span><span class="sxs-lookup"><span data-stu-id="67db2-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67db2-104">句法</span><span class="sxs-lookup"><span data-stu-id="67db2-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67db2-105">說明</span><span class="sxs-lookup"><span data-stu-id="67db2-105">DESCRIPTION</span></span>
<span data-ttu-id="67db2-106">**AzureRmDataLakeStoreItemOwner** Cmdlet 會修改 Data Lake store 中的檔案或資料夾擁有者。</span><span class="sxs-lookup"><span data-stu-id="67db2-106">The **Set-AzureRmDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="67db2-107">示例</span><span class="sxs-lookup"><span data-stu-id="67db2-107">EXAMPLES</span></span>

### <span data-ttu-id="67db2-108">範例1：設定專案的擁有者</span><span class="sxs-lookup"><span data-stu-id="67db2-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="67db2-109">這個命令會將根目錄的擁有者設定為 Patti 更完整的目錄。</span><span class="sxs-lookup"><span data-stu-id="67db2-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="67db2-110">參數</span><span class="sxs-lookup"><span data-stu-id="67db2-110">PARAMETERS</span></span>

### <span data-ttu-id="67db2-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="67db2-111">-Account</span></span>
<span data-ttu-id="67db2-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="67db2-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="67db2-113">-識別碼</span><span class="sxs-lookup"><span data-stu-id="67db2-113">-Id</span></span>
<span data-ttu-id="67db2-114">指定要作為擁有者使用之 AzureActive 目錄使用者、群組或服務主體的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="67db2-114">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

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

### <span data-ttu-id="67db2-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67db2-115">-PassThru</span></span>
<span data-ttu-id="67db2-116">指出應該傳回所產生的更新擁有者。</span><span class="sxs-lookup"><span data-stu-id="67db2-116">Indicates the resulting updated owner should be returned.</span></span>

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

### <span data-ttu-id="67db2-117">-Path</span><span class="sxs-lookup"><span data-stu-id="67db2-117">-Path</span></span>
<span data-ttu-id="67db2-118">指定要修改之專案的 Data Lake Store 路徑（從根目錄 (/) 開始）。</span><span class="sxs-lookup"><span data-stu-id="67db2-118">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="67db2-119">-類型</span><span class="sxs-lookup"><span data-stu-id="67db2-119">-Type</span></span>
<span data-ttu-id="67db2-120">指定要設定的擁有者類型。</span><span class="sxs-lookup"><span data-stu-id="67db2-120">Specifies the type of owner to set.</span></span>
<span data-ttu-id="67db2-121">此參數可接受的值為： [使用者] 和 [群組]。</span><span class="sxs-lookup"><span data-stu-id="67db2-121">The acceptable values for this parameter are: User and Group.</span></span>

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

### <span data-ttu-id="67db2-122">-確認</span><span class="sxs-lookup"><span data-stu-id="67db2-122">-Confirm</span></span>
<span data-ttu-id="67db2-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="67db2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67db2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67db2-124">-WhatIf</span></span>
<span data-ttu-id="67db2-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="67db2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67db2-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="67db2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67db2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67db2-127">-DefaultProfile</span></span>
<span data-ttu-id="67db2-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="67db2-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67db2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67db2-129">CommonParameters</span></span>
<span data-ttu-id="67db2-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="67db2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67db2-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="67db2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67db2-132">輸入</span><span class="sxs-lookup"><span data-stu-id="67db2-132">INPUTS</span></span>

## <span data-ttu-id="67db2-133">輸出</span><span class="sxs-lookup"><span data-stu-id="67db2-133">OUTPUTS</span></span>

### <span data-ttu-id="67db2-134">字串</span><span class="sxs-lookup"><span data-stu-id="67db2-134">string</span></span>
<span data-ttu-id="67db2-135">如果已指定 PassThru，則會傳回更新的擁有者。</span><span class="sxs-lookup"><span data-stu-id="67db2-135">If PassThru is specified, returns the updated owner.</span></span>

## <span data-ttu-id="67db2-136">筆記</span><span class="sxs-lookup"><span data-stu-id="67db2-136">NOTES</span></span>

## <span data-ttu-id="67db2-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="67db2-137">RELATED LINKS</span></span>

[<span data-ttu-id="67db2-138">AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="67db2-138">Get-AzureRmDataLakeStoreItemOwner</span></span>](./Get-AzureRmDataLakeStoreItemOwner.md)


