---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 00447be14fe61b76a4dbb4f62e3393bb76c1ddb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626475"
---
# <span data-ttu-id="31ba7-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="31ba7-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="31ba7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="31ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="31ba7-103">取得儲存空間帳戶的 NetWorkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="31ba7-103">Get the NetWorkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31ba7-104">句法</span><span class="sxs-lookup"><span data-stu-id="31ba7-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31ba7-105">說明</span><span class="sxs-lookup"><span data-stu-id="31ba7-105">DESCRIPTION</span></span>
<span data-ttu-id="31ba7-106">**AzureRmStorageAccountNetworkRuleSet** Cmdlet 會取得儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="31ba7-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage Account</span></span>

## <span data-ttu-id="31ba7-107">示例</span><span class="sxs-lookup"><span data-stu-id="31ba7-107">EXAMPLES</span></span>

### <span data-ttu-id="31ba7-108">範例1：取得指定儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="31ba7-108">Example 1: Get NetworkRule property of a specified storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="31ba7-109">這個命令會取得指定儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="31ba7-109">This command gets NetworkRule property of a specified storage account</span></span>

## <span data-ttu-id="31ba7-110">參數</span><span class="sxs-lookup"><span data-stu-id="31ba7-110">PARAMETERS</span></span>

### <span data-ttu-id="31ba7-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="31ba7-111">-Name</span></span>
<span data-ttu-id="31ba7-112">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="31ba7-112">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="31ba7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31ba7-113">-ResourceGroupName</span></span>
<span data-ttu-id="31ba7-114">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="31ba7-114">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="31ba7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31ba7-115">-DefaultProfile</span></span>
<span data-ttu-id="31ba7-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="31ba7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31ba7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31ba7-117">CommonParameters</span></span>
<span data-ttu-id="31ba7-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="31ba7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31ba7-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="31ba7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31ba7-120">輸入</span><span class="sxs-lookup"><span data-stu-id="31ba7-120">INPUTS</span></span>

### <span data-ttu-id="31ba7-121">System.object</span><span class="sxs-lookup"><span data-stu-id="31ba7-121">System.String</span></span>

## <span data-ttu-id="31ba7-122">輸出</span><span class="sxs-lookup"><span data-stu-id="31ba7-122">OUTPUTS</span></span>

### <span data-ttu-id="31ba7-123">PSNetworkRuleSet 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="31ba7-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="31ba7-124">筆記</span><span class="sxs-lookup"><span data-stu-id="31ba7-124">NOTES</span></span>

## <span data-ttu-id="31ba7-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="31ba7-125">RELATED LINKS</span></span>

