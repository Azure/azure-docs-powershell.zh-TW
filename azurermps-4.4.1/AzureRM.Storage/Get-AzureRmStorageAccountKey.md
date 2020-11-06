---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
ms.openlocfilehash: d12be29507f581f3e9a8d0de86d8a571a305908d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448824"
---
# <span data-ttu-id="f86ec-101">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f86ec-101">Get-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="f86ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f86ec-102">SYNOPSIS</span></span>
<span data-ttu-id="f86ec-103">取得 Azure 儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="f86ec-103">Gets the access keys for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f86ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="f86ec-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f86ec-105">說明</span><span class="sxs-lookup"><span data-stu-id="f86ec-105">DESCRIPTION</span></span>
<span data-ttu-id="f86ec-106">**AzureRmStorageAccountKey** Cmdlet 會取得 Azure 儲存空間帳戶的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="f86ec-106">The **Get-AzureRmStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="f86ec-107">示例</span><span class="sxs-lookup"><span data-stu-id="f86ec-107">EXAMPLES</span></span>

### <span data-ttu-id="f86ec-108">範例1：取得儲存空間帳戶的便捷鍵</span><span class="sxs-lookup"><span data-stu-id="f86ec-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="f86ec-109">這個命令會取得指定 Azure 儲存空間帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="f86ec-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="f86ec-110">範例2：取得儲存空間帳戶的特定便捷鍵</span><span class="sxs-lookup"><span data-stu-id="f86ec-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Value[0]

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Key1
```

## <span data-ttu-id="f86ec-111">參數</span><span class="sxs-lookup"><span data-stu-id="f86ec-111">PARAMETERS</span></span>

### <span data-ttu-id="f86ec-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="f86ec-112">-Name</span></span>
<span data-ttu-id="f86ec-113">指定此 Cmdlet 取得金鑰的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f86ec-113">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="f86ec-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f86ec-114">-ResourceGroupName</span></span>
<span data-ttu-id="f86ec-115">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f86ec-115">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="f86ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f86ec-116">-DefaultProfile</span></span>
<span data-ttu-id="f86ec-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f86ec-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f86ec-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f86ec-118">CommonParameters</span></span>
<span data-ttu-id="f86ec-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f86ec-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f86ec-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f86ec-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f86ec-121">輸入</span><span class="sxs-lookup"><span data-stu-id="f86ec-121">INPUTS</span></span>

## <span data-ttu-id="f86ec-122">輸出</span><span class="sxs-lookup"><span data-stu-id="f86ec-122">OUTPUTS</span></span>

## <span data-ttu-id="f86ec-123">筆記</span><span class="sxs-lookup"><span data-stu-id="f86ec-123">NOTES</span></span>

## <span data-ttu-id="f86ec-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="f86ec-124">RELATED LINKS</span></span>

[<span data-ttu-id="f86ec-125">新-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f86ec-125">New-AzureRmStorageAccountKey</span></span>](./New-AzureRmStorageAccountKey.md)


