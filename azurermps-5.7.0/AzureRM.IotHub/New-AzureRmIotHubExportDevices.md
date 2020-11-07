---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothubexportdevices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
ms.openlocfilehash: 2f9122b2683721aa7f92bc1695b6c314e83d76c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625897"
---
# <span data-ttu-id="8a600-101">New-AzureRmIotHubExportDevices</span><span class="sxs-lookup"><span data-stu-id="8a600-101">New-AzureRmIotHubExportDevices</span></span>

## <span data-ttu-id="8a600-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8a600-102">SYNOPSIS</span></span>
<span data-ttu-id="8a600-103">建立新的匯出裝置作業。</span><span class="sxs-lookup"><span data-stu-id="8a600-103">Creates a new export devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a600-104">句法</span><span class="sxs-lookup"><span data-stu-id="8a600-104">SYNTAX</span></span>

```
New-AzureRmIotHubExportDevices [-ResourceGroupName] <String> [-Name] <String>
 [-ExportBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a600-105">說明</span><span class="sxs-lookup"><span data-stu-id="8a600-105">DESCRIPTION</span></span>
<span data-ttu-id="8a600-106">為 IotHub 建立新的匯出裝置作業。</span><span class="sxs-lookup"><span data-stu-id="8a600-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="8a600-107">這會將所有裝置匯出至指定的容器。</span><span class="sxs-lookup"><span data-stu-id="8a600-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="8a600-108">請參閱下列文章，瞭解如何產生 SAS URI。</span><span class="sxs-lookup"><span data-stu-id="8a600-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="8a600-109"> https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span><span class="sxs-lookup"><span data-stu-id="8a600-109">https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span></span>

## <span data-ttu-id="8a600-110">示例</span><span class="sxs-lookup"><span data-stu-id="8a600-110">EXAMPLES</span></span>

### <span data-ttu-id="8a600-111">範例1發出匯出裝置要求的問題。</span><span class="sxs-lookup"><span data-stu-id="8a600-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzureRmIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys $true
```

<span data-ttu-id="8a600-112">針對 IotHub "myiothub" （不含按鍵）建立新的匯出裝置要求。</span><span class="sxs-lookup"><span data-stu-id="8a600-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="8a600-113">參數</span><span class="sxs-lookup"><span data-stu-id="8a600-113">PARAMETERS</span></span>

### <span data-ttu-id="8a600-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a600-114">-DefaultProfile</span></span>
<span data-ttu-id="8a600-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8a600-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a600-116">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="8a600-116">-ExportBlobContainerUri</span></span>
<span data-ttu-id="8a600-117">要將 blob 匯出至的 Uri。</span><span class="sxs-lookup"><span data-stu-id="8a600-117">The Uri to export the blob to.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a600-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="8a600-118">-Name</span></span>
<span data-ttu-id="8a600-119">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="8a600-119">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a600-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a600-120">-ResourceGroupName</span></span>
<span data-ttu-id="8a600-121">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="8a600-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a600-122">-確認</span><span class="sxs-lookup"><span data-stu-id="8a600-122">-Confirm</span></span>
<span data-ttu-id="8a600-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8a600-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a600-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a600-124">-WhatIf</span></span>
<span data-ttu-id="8a600-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8a600-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a600-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a600-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a600-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a600-127">CommonParameters</span></span>
<span data-ttu-id="8a600-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8a600-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a600-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8a600-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a600-130">輸入</span><span class="sxs-lookup"><span data-stu-id="8a600-130">INPUTS</span></span>

### <span data-ttu-id="8a600-131">System.object</span><span class="sxs-lookup"><span data-stu-id="8a600-131">System.String</span></span>

## <span data-ttu-id="8a600-132">輸出</span><span class="sxs-lookup"><span data-stu-id="8a600-132">OUTPUTS</span></span>

### <span data-ttu-id="8a600-133">JobResponse 中的 IotHub。</span><span class="sxs-lookup"><span data-stu-id="8a600-133">Microsoft.Azure.Management.IotHub.Models.JobResponse</span></span>

## <span data-ttu-id="8a600-134">筆記</span><span class="sxs-lookup"><span data-stu-id="8a600-134">NOTES</span></span>

## <span data-ttu-id="8a600-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a600-135">RELATED LINKS</span></span>

