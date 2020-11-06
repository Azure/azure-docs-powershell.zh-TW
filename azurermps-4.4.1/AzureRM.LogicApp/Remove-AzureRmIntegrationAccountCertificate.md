---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 71c910fafea0c555f5ba0d7a62573c2de2be3b41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453452"
---
# <span data-ttu-id="ae764-101">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ae764-101">Remove-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="ae764-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ae764-102">SYNOPSIS</span></span>
<span data-ttu-id="ae764-103">從資源群組中移除整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="ae764-103">Removes an integration account certificate from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae764-104">句法</span><span class="sxs-lookup"><span data-stu-id="ae764-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String>
 -CertificateName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae764-105">說明</span><span class="sxs-lookup"><span data-stu-id="ae764-105">DESCRIPTION</span></span>
<span data-ttu-id="ae764-106">**AzureRmIntegrationAccountCertificate** Cmdlet 會從資源群組中移除整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="ae764-106">The **Remove-AzureRmIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="ae764-107">指定整合帳戶名稱、資源群組名稱及憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="ae764-107">Specify the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="ae764-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="ae764-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ae764-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="ae764-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ae764-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="ae764-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ae764-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="ae764-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ae764-112">示例</span><span class="sxs-lookup"><span data-stu-id="ae764-112">EXAMPLES</span></span>

### <span data-ttu-id="ae764-113">範例1：移除整合帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="ae764-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="ae764-114">這個命令會移除名為 IntegrationAccount31 的 integration 帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="ae764-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="ae764-115">參數</span><span class="sxs-lookup"><span data-stu-id="ae764-115">PARAMETERS</span></span>

### <span data-ttu-id="ae764-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="ae764-116">-CertificateName</span></span>
<span data-ttu-id="ae764-117">指定整合帳戶憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae764-117">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="ae764-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ae764-118">-Force</span></span>
<span data-ttu-id="ae764-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ae764-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ae764-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="ae764-120">-Name</span></span>
<span data-ttu-id="ae764-121">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae764-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae764-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae764-122">-ResourceGroupName</span></span>
<span data-ttu-id="ae764-123">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae764-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ae764-124">-確認</span><span class="sxs-lookup"><span data-stu-id="ae764-124">-Confirm</span></span>
<span data-ttu-id="ae764-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ae764-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae764-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae764-126">-WhatIf</span></span>
<span data-ttu-id="ae764-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ae764-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae764-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ae764-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae764-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae764-129">-DefaultProfile</span></span>
<span data-ttu-id="ae764-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ae764-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae764-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae764-131">CommonParameters</span></span>
<span data-ttu-id="ae764-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ae764-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae764-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ae764-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae764-134">輸入</span><span class="sxs-lookup"><span data-stu-id="ae764-134">INPUTS</span></span>

## <span data-ttu-id="ae764-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ae764-135">OUTPUTS</span></span>

## <span data-ttu-id="ae764-136">筆記</span><span class="sxs-lookup"><span data-stu-id="ae764-136">NOTES</span></span>

## <span data-ttu-id="ae764-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae764-137">RELATED LINKS</span></span>

[<span data-ttu-id="ae764-138">AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ae764-138">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="ae764-139">新-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ae764-139">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="ae764-140">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="ae764-140">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


