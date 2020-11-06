---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchAccount.md
ms.openlocfilehash: fbf1911f7ec0483509c8a4e93f326f17c47d7f01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452587"
---
# <span data-ttu-id="a6126-101">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a6126-101">Set-AzureRmBatchAccount</span></span>

## <span data-ttu-id="a6126-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6126-102">SYNOPSIS</span></span>
<span data-ttu-id="a6126-103">更新批次帳戶。</span><span class="sxs-lookup"><span data-stu-id="a6126-103">Updates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6126-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6126-104">SYNTAX</span></span>

```
Set-AzureRmBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6126-105">說明</span><span class="sxs-lookup"><span data-stu-id="a6126-105">DESCRIPTION</span></span>
<span data-ttu-id="a6126-106">**AzureRmBatchAccount** Cmdlet 會更新 Azure Batch 帳戶。</span><span class="sxs-lookup"><span data-stu-id="a6126-106">The **Set-AzureRmBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="a6126-107">這個 Cmdlet 目前只能更新標記。</span><span class="sxs-lookup"><span data-stu-id="a6126-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="a6126-108">示例</span><span class="sxs-lookup"><span data-stu-id="a6126-108">EXAMPLES</span></span>

### <span data-ttu-id="a6126-109">範例1：更新批次帳戶上的標籤</span><span class="sxs-lookup"><span data-stu-id="a6126-109">Example 1: Update the tags on a Batch account</span></span>
```
PS C:\>Set-AzureRmBatchAccount -AccountName "cmdletexample" -Tag @{key0="value0";key1=$null;key2="value2"}
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
                               Name  Value
                               ====  ======
                               key0  value0
                               key1
                               key2  value2
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="a6126-110">這個命令會更新名為 pfuller 的帳戶上的標記。</span><span class="sxs-lookup"><span data-stu-id="a6126-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="a6126-111">參數</span><span class="sxs-lookup"><span data-stu-id="a6126-111">PARAMETERS</span></span>

### <span data-ttu-id="a6126-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a6126-112">-AccountName</span></span>
<span data-ttu-id="a6126-113">指定此 Cmdlet 更新之批次帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6126-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6126-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a6126-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="a6126-115">指定要用於自動儲存的儲存空間帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a6126-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6126-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6126-116">-ResourceGroupName</span></span>
<span data-ttu-id="a6126-117">指定此 Cmdlet 更新之帳戶的資源群組。</span><span class="sxs-lookup"><span data-stu-id="a6126-117">Specifies the resource group of the account that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6126-118">-Tag</span><span class="sxs-lookup"><span data-stu-id="a6126-118">-Tag</span></span>
<span data-ttu-id="a6126-119">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="a6126-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a6126-120">例如：</span><span class="sxs-lookup"><span data-stu-id="a6126-120">For example:</span></span>

<span data-ttu-id="a6126-121">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a6126-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6126-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6126-122">-DefaultProfile</span></span>
<span data-ttu-id="a6126-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6126-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6126-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6126-124">CommonParameters</span></span>
<span data-ttu-id="a6126-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6126-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6126-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a6126-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6126-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a6126-127">INPUTS</span></span>

## <span data-ttu-id="a6126-128">輸出</span><span class="sxs-lookup"><span data-stu-id="a6126-128">OUTPUTS</span></span>

### <span data-ttu-id="a6126-129">BatchAccountCoNtext</span><span class="sxs-lookup"><span data-stu-id="a6126-129">BatchAccountContext</span></span>

## <span data-ttu-id="a6126-130">筆記</span><span class="sxs-lookup"><span data-stu-id="a6126-130">NOTES</span></span>

## <span data-ttu-id="a6126-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6126-131">RELATED LINKS</span></span>

[<span data-ttu-id="a6126-132">AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a6126-132">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="a6126-133">新-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a6126-133">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="a6126-134">移除-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="a6126-134">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="a6126-135">Azure 批次 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a6126-135">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
