---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/disable-azstoragedeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageDeleteRetentionPolicy.md
ms.openlocfilehash: dac884a0faf44380f19447f2d52af1e172feb9a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907270"
---
# <span data-ttu-id="9eb23-101">Disable-AzStorageDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="9eb23-101">Disable-AzStorageDeleteRetentionPolicy</span></span>

## <span data-ttu-id="9eb23-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9eb23-102">SYNOPSIS</span></span>
<span data-ttu-id="9eb23-103">停用 Azure 儲存體 Blob 服務的刪除保留政策。</span><span class="sxs-lookup"><span data-stu-id="9eb23-103">Disable delete retention policy  for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="9eb23-104">語法</span><span class="sxs-lookup"><span data-stu-id="9eb23-104">SYNTAX</span></span>

```
Disable-AzStorageDeleteRetentionPolicy [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9eb23-105">描述</span><span class="sxs-lookup"><span data-stu-id="9eb23-105">DESCRIPTION</span></span>
<span data-ttu-id="9eb23-106">**Disable-AzStorageDeleteRetentionPolicy** Cmdlet 會停用 Azure 儲存體 Blob 服務的刪除保留原則。</span><span class="sxs-lookup"><span data-stu-id="9eb23-106">The **Disable-AzStorageDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="9eb23-107">例子</span><span class="sxs-lookup"><span data-stu-id="9eb23-107">EXAMPLES</span></span>

### <span data-ttu-id="9eb23-108">範例 1：停用 Blob 服務的刪除保留政策</span><span class="sxs-lookup"><span data-stu-id="9eb23-108">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageDeleteRetentionPolicy
```

<span data-ttu-id="9eb23-109">此命令會停用 Blob 服務的刪除保留原則。</span><span class="sxs-lookup"><span data-stu-id="9eb23-109">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="9eb23-110">參數</span><span class="sxs-lookup"><span data-stu-id="9eb23-110">PARAMETERS</span></span>

### <span data-ttu-id="9eb23-111">-內容</span><span class="sxs-lookup"><span data-stu-id="9eb23-111">-Context</span></span>
<span data-ttu-id="9eb23-112">Azure 儲存體內容物件</span><span class="sxs-lookup"><span data-stu-id="9eb23-112">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9eb23-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eb23-113">-DefaultProfile</span></span>
<span data-ttu-id="9eb23-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9eb23-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb23-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9eb23-115">-PassThru</span></span>
<span data-ttu-id="9eb23-116">顯示 DeleteRetentionPolicyProperties</span><span class="sxs-lookup"><span data-stu-id="9eb23-116">Display DeleteRetentionPolicyProperties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb23-117">-確認</span><span class="sxs-lookup"><span data-stu-id="9eb23-117">-Confirm</span></span>
<span data-ttu-id="9eb23-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9eb23-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb23-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eb23-119">-WhatIf</span></span>
<span data-ttu-id="9eb23-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9eb23-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eb23-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9eb23-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9eb23-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eb23-122">CommonParameters</span></span>
<span data-ttu-id="9eb23-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9eb23-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eb23-124">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="9eb23-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eb23-125">輸入</span><span class="sxs-lookup"><span data-stu-id="9eb23-125">INPUTS</span></span>

### <span data-ttu-id="9eb23-126">Microsoft.Azure.Commands.Common.Authentication.Azs.IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="9eb23-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9eb23-127">輸出</span><span class="sxs-lookup"><span data-stu-id="9eb23-127">OUTPUTS</span></span>

### <span data-ttu-id="9eb23-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="9eb23-128">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="9eb23-129">筆記</span><span class="sxs-lookup"><span data-stu-id="9eb23-129">NOTES</span></span>

## <span data-ttu-id="9eb23-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="9eb23-130">RELATED LINKS</span></span>
