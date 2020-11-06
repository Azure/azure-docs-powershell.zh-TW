---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 30C10687-F172-4663-8D4A-F0DDEA5C3741
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoretrustedidprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreTrustedIdProvider.md
ms.openlocfilehash: c769e3e084f0ac5fd6df22bae81a4d8df99dc700
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456231"
---
# <span data-ttu-id="815af-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span><span class="sxs-lookup"><span data-stu-id="815af-101">Remove-AzureRmDataLakeStoreTrustedIdProvider</span></span>

## <span data-ttu-id="815af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="815af-102">SYNOPSIS</span></span>
<span data-ttu-id="815af-103">移除指定資料 Lake Store 中指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="815af-103">Removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="815af-104">句法</span><span class="sxs-lookup"><span data-stu-id="815af-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreTrustedIdProvider [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="815af-105">說明</span><span class="sxs-lookup"><span data-stu-id="815af-105">DESCRIPTION</span></span>
<span data-ttu-id="815af-106">**AzureRmDataLakeStoreTrustedIdProvider** Cmdlet 會在指定的 Data Lake store 中移除指定的信任身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="815af-106">The **Remove-AzureRmDataLakeStoreTrustedIdProvider** cmdlet removes the specified trusted identity provider in the specified Data Lake Store.</span></span>

## <span data-ttu-id="815af-107">示例</span><span class="sxs-lookup"><span data-stu-id="815af-107">EXAMPLES</span></span>

### <span data-ttu-id="815af-108">範例1：移除信任的身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="815af-108">Example 1: Remove a trusted identity provider.</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreTrustedIdProvider -AccountName "ContosoADL" -Name MyProvider
```

<span data-ttu-id="815af-109">從帳戶 "ContosoADL" 移除提供者 "MyProvider"</span><span class="sxs-lookup"><span data-stu-id="815af-109">Removes the provider "MyProvider" from account "ContosoADL"</span></span>

## <span data-ttu-id="815af-110">參數</span><span class="sxs-lookup"><span data-stu-id="815af-110">PARAMETERS</span></span>

### <span data-ttu-id="815af-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="815af-111">-Account</span></span>
<span data-ttu-id="815af-112">要從中移除信任身分識別提供者的 Data Lake Store 帳戶</span><span class="sxs-lookup"><span data-stu-id="815af-112">The Data Lake Store account to remove the trusted identity provider from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="815af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="815af-113">-DefaultProfile</span></span>
<span data-ttu-id="815af-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="815af-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="815af-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="815af-115">-Name</span></span>
<span data-ttu-id="815af-116">信任身分識別提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="815af-116">The name of the trusted identity provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="815af-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="815af-117">-PassThru</span></span>
<span data-ttu-id="815af-118">表示應傳回指示刪除操作結果的布林回應。</span><span class="sxs-lookup"><span data-stu-id="815af-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="815af-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="815af-119">-ResourceGroupName</span></span>
<span data-ttu-id="815af-120">指定包含要從中移除信任身分識別提供者之帳戶的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="815af-120">Specifies the name of the resource group that contains the account to remove the trusted identity provider from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="815af-121">-確認</span><span class="sxs-lookup"><span data-stu-id="815af-121">-Confirm</span></span>
<span data-ttu-id="815af-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="815af-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="815af-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="815af-123">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="815af-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="815af-124">CommonParameters</span></span>
<span data-ttu-id="815af-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="815af-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="815af-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="815af-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="815af-127">輸入</span><span class="sxs-lookup"><span data-stu-id="815af-127">INPUTS</span></span>

### <span data-ttu-id="815af-128">所有</span><span class="sxs-lookup"><span data-stu-id="815af-128">None</span></span>
<span data-ttu-id="815af-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="815af-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="815af-130">輸出</span><span class="sxs-lookup"><span data-stu-id="815af-130">OUTPUTS</span></span>

### <span data-ttu-id="815af-131">bool</span><span class="sxs-lookup"><span data-stu-id="815af-131">bool</span></span>
<span data-ttu-id="815af-132">如果已指定 PassThru，則會在成功完成時傳回 true。</span><span class="sxs-lookup"><span data-stu-id="815af-132">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="815af-133">筆記</span><span class="sxs-lookup"><span data-stu-id="815af-133">NOTES</span></span>

## <span data-ttu-id="815af-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="815af-134">RELATED LINKS</span></span>

