---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 6dbb2342673a35b73ead97eef50bc58a65ccfd19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915146"
---
# <span data-ttu-id="9eec1-101">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9eec1-101">Get-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="9eec1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9eec1-102">SYNOPSIS</span></span>
<span data-ttu-id="9eec1-103">取得儲存空間帳戶的 NetWorkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="9eec1-103">Get the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="9eec1-104">語法</span><span class="sxs-lookup"><span data-stu-id="9eec1-104">SYNTAX</span></span>

```
Get-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9eec1-105">描述</span><span class="sxs-lookup"><span data-stu-id="9eec1-105">DESCRIPTION</span></span>
<span data-ttu-id="9eec1-106">**Get-AzStorageAccountNetworkRuleSet** Cmdlet 取得儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="9eec1-106">The **Get-AzStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="9eec1-107">例子</span><span class="sxs-lookup"><span data-stu-id="9eec1-107">EXAMPLES</span></span>

### <span data-ttu-id="9eec1-108">範例 1：取得指定儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="9eec1-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="9eec1-109">此命令會獲得指定儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="9eec1-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="9eec1-110">參數</span><span class="sxs-lookup"><span data-stu-id="9eec1-110">PARAMETERS</span></span>

### <span data-ttu-id="9eec1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eec1-111">-DefaultProfile</span></span>
<span data-ttu-id="9eec1-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9eec1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9eec1-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="9eec1-113">-Name</span></span>
<span data-ttu-id="9eec1-114">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="9eec1-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="9eec1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eec1-115">-ResourceGroupName</span></span>
<span data-ttu-id="9eec1-116">指定包含儲存空間帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="9eec1-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="9eec1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eec1-117">CommonParameters</span></span>
<span data-ttu-id="9eec1-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9eec1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eec1-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9eec1-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eec1-120">輸入</span><span class="sxs-lookup"><span data-stu-id="9eec1-120">INPUTS</span></span>

### <span data-ttu-id="9eec1-121">System.String</span><span class="sxs-lookup"><span data-stu-id="9eec1-121">System.String</span></span>

## <span data-ttu-id="9eec1-122">輸出</span><span class="sxs-lookup"><span data-stu-id="9eec1-122">OUTPUTS</span></span>

### <span data-ttu-id="9eec1-123">Microsoft.Azure.Commands.management.storage.models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9eec1-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="9eec1-124">筆記</span><span class="sxs-lookup"><span data-stu-id="9eec1-124">NOTES</span></span>

## <span data-ttu-id="9eec1-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="9eec1-125">RELATED LINKS</span></span>
