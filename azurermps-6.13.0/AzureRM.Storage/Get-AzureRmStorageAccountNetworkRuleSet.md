---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 0a316ee8e4d1d7c8d58e2444aa6cdfadbc5e0367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448871"
---
# <span data-ttu-id="547eb-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="547eb-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="547eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="547eb-102">SYNOPSIS</span></span>
<span data-ttu-id="547eb-103">取得儲存空間帳戶的 NetWorkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="547eb-103">Get the NetWorkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="547eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="547eb-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="547eb-105">說明</span><span class="sxs-lookup"><span data-stu-id="547eb-105">DESCRIPTION</span></span>
<span data-ttu-id="547eb-106">**AzureRmStorageAccountNetworkRuleSet** Cmdlet 會取得儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="547eb-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="547eb-107">示例</span><span class="sxs-lookup"><span data-stu-id="547eb-107">EXAMPLES</span></span>

### <span data-ttu-id="547eb-108">範例1：取得指定儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="547eb-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="547eb-109">這個命令會取得指定儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="547eb-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="547eb-110">參數</span><span class="sxs-lookup"><span data-stu-id="547eb-110">PARAMETERS</span></span>

### <span data-ttu-id="547eb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="547eb-111">-DefaultProfile</span></span>
<span data-ttu-id="547eb-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="547eb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="547eb-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="547eb-113">-Name</span></span>
<span data-ttu-id="547eb-114">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="547eb-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="547eb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="547eb-115">-ResourceGroupName</span></span>
<span data-ttu-id="547eb-116">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="547eb-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="547eb-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="547eb-117">CommonParameters</span></span>
<span data-ttu-id="547eb-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="547eb-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="547eb-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="547eb-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="547eb-120">輸入</span><span class="sxs-lookup"><span data-stu-id="547eb-120">INPUTS</span></span>

### <span data-ttu-id="547eb-121">System.object</span><span class="sxs-lookup"><span data-stu-id="547eb-121">System.String</span></span>

## <span data-ttu-id="547eb-122">輸出</span><span class="sxs-lookup"><span data-stu-id="547eb-122">OUTPUTS</span></span>

### <span data-ttu-id="547eb-123">PSNetworkRuleSet 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="547eb-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="547eb-124">筆記</span><span class="sxs-lookup"><span data-stu-id="547eb-124">NOTES</span></span>

## <span data-ttu-id="547eb-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="547eb-125">RELATED LINKS</span></span>
