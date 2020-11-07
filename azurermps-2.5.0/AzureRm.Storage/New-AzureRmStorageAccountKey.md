---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstorageaccountkey
schema: 2.0.0
ms.openlocfilehash: 7ea3847c011582d9be809f030a638b09b6cf9532
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93799713"
---
# <span data-ttu-id="5aa93-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="5aa93-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="5aa93-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5aa93-102">SYNOPSIS</span></span>
<span data-ttu-id="5aa93-103">重新產生 Azure 儲存空間帳戶的儲存金鑰。</span><span class="sxs-lookup"><span data-stu-id="5aa93-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5aa93-104">句法</span><span class="sxs-lookup"><span data-stu-id="5aa93-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5aa93-105">說明</span><span class="sxs-lookup"><span data-stu-id="5aa93-105">DESCRIPTION</span></span>
<span data-ttu-id="5aa93-106">**新的-AzureRmStorageAccountKey** Cmdlet 會為 Azure 儲存空間帳戶重新產生儲存空間金鑰。</span><span class="sxs-lookup"><span data-stu-id="5aa93-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="5aa93-107">示例</span><span class="sxs-lookup"><span data-stu-id="5aa93-107">EXAMPLES</span></span>

### <span data-ttu-id="5aa93-108">範例1：重新產生儲存金鑰</span><span class="sxs-lookup"><span data-stu-id="5aa93-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="5aa93-109">這個命令會為指定的儲存空間帳戶重新生成儲存空間。</span><span class="sxs-lookup"><span data-stu-id="5aa93-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="5aa93-110">參數</span><span class="sxs-lookup"><span data-stu-id="5aa93-110">PARAMETERS</span></span>

### <span data-ttu-id="5aa93-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aa93-111">-DefaultProfile</span></span>
<span data-ttu-id="5aa93-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5aa93-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5aa93-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="5aa93-113">-KeyName</span></span>
<span data-ttu-id="5aa93-114">指定要重新產生的金鑰。</span><span class="sxs-lookup"><span data-stu-id="5aa93-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="5aa93-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5aa93-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5aa93-116">key1</span><span class="sxs-lookup"><span data-stu-id="5aa93-116">key1</span></span>
- <span data-ttu-id="5aa93-117">key2</span><span class="sxs-lookup"><span data-stu-id="5aa93-117">key2</span></span>

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

### <span data-ttu-id="5aa93-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="5aa93-118">-Name</span></span>
<span data-ttu-id="5aa93-119">指定要重新產生儲存金鑰的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="5aa93-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

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

### <span data-ttu-id="5aa93-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aa93-120">-ResourceGroupName</span></span>
<span data-ttu-id="5aa93-121">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5aa93-121">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="5aa93-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aa93-122">CommonParameters</span></span>
<span data-ttu-id="5aa93-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5aa93-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aa93-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5aa93-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aa93-125">輸入</span><span class="sxs-lookup"><span data-stu-id="5aa93-125">INPUTS</span></span>

### <span data-ttu-id="5aa93-126">System.object</span><span class="sxs-lookup"><span data-stu-id="5aa93-126">System.String</span></span>

## <span data-ttu-id="5aa93-127">輸出</span><span class="sxs-lookup"><span data-stu-id="5aa93-127">OUTPUTS</span></span>

### <span data-ttu-id="5aa93-128">StorageAccountKey （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="5aa93-128">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="5aa93-129">筆記</span><span class="sxs-lookup"><span data-stu-id="5aa93-129">NOTES</span></span>

## <span data-ttu-id="5aa93-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="5aa93-130">RELATED LINKS</span></span>

[<span data-ttu-id="5aa93-131">AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="5aa93-131">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)
