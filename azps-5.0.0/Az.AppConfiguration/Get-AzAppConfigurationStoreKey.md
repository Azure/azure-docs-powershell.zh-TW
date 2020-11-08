---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstorekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStoreKey.md
ms.openlocfilehash: b33827640108077504b3142b58a1d8a71c8ffc95
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137586"
---
# <span data-ttu-id="0b057-101">Get-AzAppConfigurationStoreKey</span><span class="sxs-lookup"><span data-stu-id="0b057-101">Get-AzAppConfigurationStoreKey</span></span>

## <span data-ttu-id="0b057-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0b057-102">SYNOPSIS</span></span>
<span data-ttu-id="0b057-103">列出指定的配置存放區的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="0b057-103">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="0b057-104">句法</span><span class="sxs-lookup"><span data-stu-id="0b057-104">SYNTAX</span></span>

```
Get-AzAppConfigurationStoreKey -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0b057-105">說明</span><span class="sxs-lookup"><span data-stu-id="0b057-105">DESCRIPTION</span></span>
<span data-ttu-id="0b057-106">列出指定的配置存放區的便捷鍵。</span><span class="sxs-lookup"><span data-stu-id="0b057-106">Lists the access key for the specified configuration store.</span></span>

## <span data-ttu-id="0b057-107">示例</span><span class="sxs-lookup"><span data-stu-id="0b057-107">EXAMPLES</span></span>

### <span data-ttu-id="0b057-108">範例1：列出 app 配置存放區的所有商店金鑰</span><span class="sxs-lookup"><span data-stu-id="0b057-108">Example 1: List all store keys of an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStoreKey -Name appconfig-test01 -ResourceGroupName azpwsh-manual-test

ConnectionString                                                                                                                     LastModified        Name                ReadOnly Value
----------------                                                                                                                     ------------        ----                -------- -----
Endpoint=https://appconfig-test01.azconfig.io;Id=TvV0-l0-s0:osSixtp4xggJYFlsJyYl;Secret=Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5kRbc= 5/7/2020 9:09:27 AM Primary             False    Bfxnosrs952PTGxvb2bdFtlTDCBPFDTlBATuEO5k...
Endpoint=https://appconfig-test01.azconfig.io;Id=gcxl-l0-s0:JfSn6JA9UFkRj7/3GVTu;Secret=0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx6X0= 5/7/2020 9:09:27 AM Secondary           False    0fH4qQ+LLvKUKEiT3kICQTEbV0WNMi4xNu9RZxPx...
Endpoint=https://appconfig-test01.azconfig.io;Id=Sl1p-l0-s0:jVozhIOYoXZ9k5pCjWa2;Secret=bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE9Ik= 5/7/2020 9:09:27 AM Primary Read Only   True     bAmj8BqcHguVraXNAJfuD1bDR+gzlfk2hf8ZSZhE...
Endpoint=https://appconfig-test01.azconfig.io;Id=htND-l0-s0:GN83PmhOFYlAlcXHN2/6;Secret=n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgcSMQ= 5/7/2020 9:09:27 AM Secondary Read Only True     n2tp5evU2F4Z1QkctG2TgZkgMxojEkod3KTEaEgc...
```

<span data-ttu-id="0b057-109">這個命令會列出 app 配置存放區的所有商店金鑰。</span><span class="sxs-lookup"><span data-stu-id="0b057-109">This command lists all store keys of an app configuration store.</span></span>

## <span data-ttu-id="0b057-110">參數</span><span class="sxs-lookup"><span data-stu-id="0b057-110">PARAMETERS</span></span>

### <span data-ttu-id="0b057-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b057-111">-DefaultProfile</span></span>
<span data-ttu-id="0b057-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0b057-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b057-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="0b057-113">-Name</span></span>
<span data-ttu-id="0b057-114">配置存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b057-114">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b057-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b057-115">-ResourceGroupName</span></span>
<span data-ttu-id="0b057-116">容器註冊表所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0b057-116">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b057-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0b057-117">-SubscriptionId</span></span>
<span data-ttu-id="0b057-118">Microsoft Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="0b057-118">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b057-119">-確認</span><span class="sxs-lookup"><span data-stu-id="0b057-119">-Confirm</span></span>
<span data-ttu-id="0b057-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0b057-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b057-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b057-121">-WhatIf</span></span>
<span data-ttu-id="0b057-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0b057-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b057-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0b057-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b057-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b057-124">CommonParameters</span></span>
<span data-ttu-id="0b057-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0b057-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b057-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0b057-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b057-127">輸入</span><span class="sxs-lookup"><span data-stu-id="0b057-127">INPUTS</span></span>

## <span data-ttu-id="0b057-128">輸出</span><span class="sxs-lookup"><span data-stu-id="0b057-128">OUTPUTS</span></span>

### <span data-ttu-id="0b057-129">IApiKey （AppConfiguration）。 Api20200601。</span><span class="sxs-lookup"><span data-stu-id="0b057-129">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IApiKey</span></span>

## <span data-ttu-id="0b057-130">筆記</span><span class="sxs-lookup"><span data-stu-id="0b057-130">NOTES</span></span>

<span data-ttu-id="0b057-131">別名</span><span class="sxs-lookup"><span data-stu-id="0b057-131">ALIASES</span></span>

## <span data-ttu-id="0b057-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="0b057-132">RELATED LINKS</span></span>

