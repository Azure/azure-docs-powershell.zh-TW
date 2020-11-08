---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountcallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCallbackUrl.md
ms.openlocfilehash: 91a61935552258e5ca52ded6e05729deecaf5665
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140102"
---
# <span data-ttu-id="bbb5a-101">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="bbb5a-101">Get-AzIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="bbb5a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bbb5a-102">SYNOPSIS</span></span>
<span data-ttu-id="bbb5a-103">取得整合帳戶回撥 URL。</span><span class="sxs-lookup"><span data-stu-id="bbb5a-103">Gets an integration account callback URL.</span></span>

## <span data-ttu-id="bbb5a-104">句法</span><span class="sxs-lookup"><span data-stu-id="bbb5a-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbb5a-105">說明</span><span class="sxs-lookup"><span data-stu-id="bbb5a-105">DESCRIPTION</span></span>
<span data-ttu-id="bbb5a-106">**AzIntegrationAccountCallbackUrl** Cmdlet 會從資源群組取得整合帳戶回撥 URL。</span><span class="sxs-lookup"><span data-stu-id="bbb5a-106">The **Get-AzIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="bbb5a-107">這個 Cmdlet 會傳回代表整合帳戶回撥 URL 的 **CallbackUrl** 物件。</span><span class="sxs-lookup"><span data-stu-id="bbb5a-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="bbb5a-108">指定整合帳戶名稱和資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="bbb5a-108">Specify the integration account name and resource group name.</span></span>
<span data-ttu-id="bbb5a-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="bbb5a-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="bbb5a-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="bbb5a-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="bbb5a-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="bbb5a-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="bbb5a-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="bbb5a-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="bbb5a-113">示例</span><span class="sxs-lookup"><span data-stu-id="bbb5a-113">EXAMPLES</span></span>

### <span data-ttu-id="bbb5a-114">範例1：取得整合帳戶回撥 URL</span><span class="sxs-lookup"><span data-stu-id="bbb5a-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="bbb5a-115">這個命令會取得整合帳戶回撥 URL。</span><span class="sxs-lookup"><span data-stu-id="bbb5a-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="bbb5a-116">參數</span><span class="sxs-lookup"><span data-stu-id="bbb5a-116">PARAMETERS</span></span>

### <span data-ttu-id="bbb5a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbb5a-117">-DefaultProfile</span></span>
<span data-ttu-id="bbb5a-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bbb5a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbb5a-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="bbb5a-119">-Name</span></span>
<span data-ttu-id="bbb5a-120">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="bbb5a-120">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbb5a-121">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="bbb5a-121">-NotAfter</span></span>
<span data-ttu-id="bbb5a-122">指定回撥 URL 的到期日。</span><span class="sxs-lookup"><span data-stu-id="bbb5a-122">Specifies the expiry date for the callback URL.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbb5a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbb5a-123">-ResourceGroupName</span></span>
<span data-ttu-id="bbb5a-124">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bbb5a-124">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbb5a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbb5a-125">CommonParameters</span></span>
<span data-ttu-id="bbb5a-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bbb5a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbb5a-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bbb5a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbb5a-128">輸入</span><span class="sxs-lookup"><span data-stu-id="bbb5a-128">INPUTS</span></span>

### <span data-ttu-id="bbb5a-129">System.object</span><span class="sxs-lookup"><span data-stu-id="bbb5a-129">System.String</span></span>

## <span data-ttu-id="bbb5a-130">輸出</span><span class="sxs-lookup"><span data-stu-id="bbb5a-130">OUTPUTS</span></span>

### <span data-ttu-id="bbb5a-131">CallbackUrl 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="bbb5a-131">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="bbb5a-132">筆記</span><span class="sxs-lookup"><span data-stu-id="bbb5a-132">NOTES</span></span>

## <span data-ttu-id="bbb5a-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="bbb5a-133">RELATED LINKS</span></span>

[<span data-ttu-id="bbb5a-134">AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="bbb5a-134">Get-AzLogicAppTriggerCallbackUrl</span></span>](./Get-AzLogicAppTriggerCallbackUrl.md)

