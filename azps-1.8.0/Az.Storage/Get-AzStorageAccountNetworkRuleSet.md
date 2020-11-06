---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 5b269eef98072a7daaaf21aa0160167bb714c77a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614623"
---
# <span data-ttu-id="155af-101">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="155af-101">Get-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="155af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="155af-102">SYNOPSIS</span></span>
<span data-ttu-id="155af-103">取得儲存空間帳戶的 NetWorkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="155af-103">Get the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="155af-104">句法</span><span class="sxs-lookup"><span data-stu-id="155af-104">SYNTAX</span></span>

```
Get-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="155af-105">說明</span><span class="sxs-lookup"><span data-stu-id="155af-105">DESCRIPTION</span></span>
<span data-ttu-id="155af-106">**AzStorageAccountNetworkRuleSet** Cmdlet 會取得儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="155af-106">The **Get-AzStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="155af-107">示例</span><span class="sxs-lookup"><span data-stu-id="155af-107">EXAMPLES</span></span>

### <span data-ttu-id="155af-108">範例1：取得指定儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="155af-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="155af-109">這個命令會取得指定儲存空間帳戶的 NetworkRule 屬性</span><span class="sxs-lookup"><span data-stu-id="155af-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="155af-110">參數</span><span class="sxs-lookup"><span data-stu-id="155af-110">PARAMETERS</span></span>

### <span data-ttu-id="155af-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="155af-111">-DefaultProfile</span></span>
<span data-ttu-id="155af-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="155af-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="155af-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="155af-113">-Name</span></span>
<span data-ttu-id="155af-114">指定儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="155af-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="155af-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="155af-115">-ResourceGroupName</span></span>
<span data-ttu-id="155af-116">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="155af-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="155af-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="155af-117">CommonParameters</span></span>
<span data-ttu-id="155af-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="155af-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="155af-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="155af-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="155af-120">輸入</span><span class="sxs-lookup"><span data-stu-id="155af-120">INPUTS</span></span>

### <span data-ttu-id="155af-121">System.object</span><span class="sxs-lookup"><span data-stu-id="155af-121">System.String</span></span>

## <span data-ttu-id="155af-122">輸出</span><span class="sxs-lookup"><span data-stu-id="155af-122">OUTPUTS</span></span>

### <span data-ttu-id="155af-123">PSNetworkRuleSet 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="155af-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="155af-124">筆記</span><span class="sxs-lookup"><span data-stu-id="155af-124">NOTES</span></span>

## <span data-ttu-id="155af-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="155af-125">RELATED LINKS</span></span>
