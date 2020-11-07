---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: 05bd6c804d359a06e83f25922263bdfdb55acc73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793064"
---
# <span data-ttu-id="954d7-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="954d7-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="954d7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="954d7-102">SYNOPSIS</span></span>
<span data-ttu-id="954d7-103">重新產生 Azure 儲存空間帳戶的儲存金鑰。</span><span class="sxs-lookup"><span data-stu-id="954d7-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="954d7-104">句法</span><span class="sxs-lookup"><span data-stu-id="954d7-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="954d7-105">說明</span><span class="sxs-lookup"><span data-stu-id="954d7-105">DESCRIPTION</span></span>
<span data-ttu-id="954d7-106">**新的-AzStorageAccountKey** Cmdlet 會為 Azure 儲存空間帳戶重新產生儲存空間金鑰。</span><span class="sxs-lookup"><span data-stu-id="954d7-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="954d7-107">示例</span><span class="sxs-lookup"><span data-stu-id="954d7-107">EXAMPLES</span></span>

### <span data-ttu-id="954d7-108">範例1：重新產生儲存金鑰</span><span class="sxs-lookup"><span data-stu-id="954d7-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="954d7-109">這個命令會為指定的儲存空間帳戶重新生成儲存空間。</span><span class="sxs-lookup"><span data-stu-id="954d7-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="954d7-110">參數</span><span class="sxs-lookup"><span data-stu-id="954d7-110">PARAMETERS</span></span>

### <span data-ttu-id="954d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="954d7-111">-DefaultProfile</span></span>
<span data-ttu-id="954d7-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="954d7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="954d7-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="954d7-113">-KeyName</span></span>
<span data-ttu-id="954d7-114">指定要重新產生的金鑰。</span><span class="sxs-lookup"><span data-stu-id="954d7-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="954d7-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="954d7-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="954d7-116">key1</span><span class="sxs-lookup"><span data-stu-id="954d7-116">key1</span></span>
- <span data-ttu-id="954d7-117">key2</span><span class="sxs-lookup"><span data-stu-id="954d7-117">key2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="954d7-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="954d7-118">-Name</span></span>
<span data-ttu-id="954d7-119">指定要重新產生儲存金鑰的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="954d7-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="954d7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="954d7-120">-ResourceGroupName</span></span>
<span data-ttu-id="954d7-121">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="954d7-121">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="954d7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="954d7-122">CommonParameters</span></span>
<span data-ttu-id="954d7-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="954d7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="954d7-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="954d7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="954d7-125">輸入</span><span class="sxs-lookup"><span data-stu-id="954d7-125">INPUTS</span></span>

### <span data-ttu-id="954d7-126">System.object</span><span class="sxs-lookup"><span data-stu-id="954d7-126">System.String</span></span>

## <span data-ttu-id="954d7-127">輸出</span><span class="sxs-lookup"><span data-stu-id="954d7-127">OUTPUTS</span></span>

### <span data-ttu-id="954d7-128">StorageAccountKey （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="954d7-128">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="954d7-129">筆記</span><span class="sxs-lookup"><span data-stu-id="954d7-129">NOTES</span></span>

## <span data-ttu-id="954d7-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="954d7-130">RELATED LINKS</span></span>

[<span data-ttu-id="954d7-131">AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="954d7-131">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
